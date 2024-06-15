1. Enumerate all machine ports

2. Enumerate page directories

3. Go on and try some injections in the search function of the page presented in the main page

4. After trying some things like XSS injection or SQLi you'll end up trying a SSTI attack and, because of the info the page gives when something fails you may elucidate the template name by just googling (SpringFramework)

5. Once you've obtained the info about the template engine you can search for a SSTI exploit that suits and you'll come across one of the ones listed in [[SSTI - Server Side Template Injection]]. The one used in the machine was the one which used `.concat(T(java.lang.Character).toString(97))`. The code written to make everything easier is listed in the [[RedPanda - Code]] note.

6. Now that you're inside the machine you have to enumerate every possible escalation way listed in [[Own machine enum]], after doing this you'll have to run pspy in order to discover a jar file being run by root in the directory `/opt/credit-score/LogParser/final/target/final-1.0-jar-with-dependencies.jar`
	1. Another way to come to this conclution is to run the command `ps -faux` and enumerate some files in the `/opt/panda_search` dir for `woodenk` by using the command `grep -r woodenk /opt/panda_search/ 2>/dev/null`

One way:

7. After seeing this, your next movement should be start a server in the victim's machine and send the jar file to your machine in order to examine it with `jd-gui`. This can be done with [[Ways to pass files from a machine to other]].

8. Another thing worth mentioning is that if you list all the files you've privilege in you'll find out that, because you're in the logs group, you've access to the file `/opt/panda_search/redpanda.log` that luckily runs in the jar file

9. Now, you've to do some code analysis in order to know exactly what the java app does. Once you've done this you are able to try to exploit the code with a simple XXE using an already existing XML file of the victim's machine and some path traversal techniques

The other way: 

7. After running the "home-made" pspy you'll come up with a possible way of escalating privileges, this way is to manipulate the redpanda.log file that is being created by root in a way that we could end up using our requests to insert some kind of input. In order to find a way to do this you can run `grep -r redpanda.log 2>/dev/null` with the purpose of finding files or scripts that name the file in at least one line

8. Now that we've found the file that may enable us to become root (``/opt/credit-score/LogParser/final/src/main/java/com/logparser/App.java``) we've to analyze it in order to find the way to exploit it

9. After analyzing the code we will come to the conclusion that the code does the follows these steps:
	1. Firstly it opens the file redpanda.log and copies its content into a variable
	2. Right after that it splits the code into 4 areas: status_code, ip, user_agent and URI. This is done by splitting it with the "||" pattern, so, because we've control over the user agent we can run the command curl to affect the way that the user_agent and, by mistake, the URI behaves
	3. After this the app reads all the lines one by one and, by the usage of another function, it verifies if the URI contains the extension .jpg, if not the program stops
	4. The following step is to save the URI and paste it in the following path: `/opt/panda_search/src/main/resources/static + URI`. Because of this, we can try to change the URI into a path traversal to make the app retrieve a .jpg file we've in an accessible directory for us like `/tmp` with the following user-agent `nothing||/../../../../../../../../../../img.jpg`. The final CURL command is: `curl -A "nothing||/../../../../../../../../../../img.jpg" 10.10.11.170:8080`
	5. Now that we have modified the redpanda.log to make the URI change to something more favourable we have to continue making some changes in our favour following the command behaviour
	6. After doing all these steps the app gets the metadata of the file specified (`img.jpg` in our case) and seeks for "Artist" to, later on, make a file called "(Artist)\_creds.xml" in the /credits directory. In order to exploit this step we've to, locally, download an image from the page and, with the help of the exiftool tool, chage its metadata to match our needs (The command necessary to do this is: `exiftool img.jpg -Artist:"/../../../../tmp/xxe"`) in order to make the app look for the file `xxe_creds.xml`. Once all this job is done, the only thing you need to do is to upload this file to the victim's computer via a simple download like the one shown in [[Ways to pass files from a machine to other]] with python server locally and wget in the victim's machine
	7. Now, the last step we've to do is a simple xxe in order to make the app show us a sensitive file when it tries to read what is in the file in the `/tmp/xxe_creds.xml` path. The structure of the file refered to previously is:
	```
	<?xml version="1.0" encoding="UTF-8"?>
	<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///root/.ssh/id_rsa"> ]>
	<stock>&xxe;</stock>
	```
	8. Right after we've all set up the only thing we need to do is send the request with the changed User-Agent and use the command `watch -n 1 cat xxe_creds.xml` in order to be notified when the file changes from the thing shown above to the ssh private key of the root user

10. Now that you've full understanding of what the code does and you've the private key in your hands, the only thing you need to do is paste it inside a file, give the file 600 permissons `chmod 600 id_rsa` and use it as an identification file with the command `ssh root@10.10.11.170 -i id_rsa`