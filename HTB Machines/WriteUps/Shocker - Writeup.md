1. Enumerate the ports with Nmap

2. Look for possible exploits to the versions of the services running on the server

3. Enumerate all the directories and files using the [GoBuster](</General Info/Tools/Enumeracion/GoBuster.md>) tool. 
	Usage: gobuster dir --wordlist __{wordlist ex. directory-list}__ -u __{Url}__ __{IP}__

4. Once you've finished to enumerate all the directories you can see that there is a rare directory called /cgi-bin/ that contains some cgi scripts

5. Because of the existence of this scripts you can try to execute an exploit from the family of exploits called Shellshock, this exploits enables you to attack some implementations of web servers that use Bash for certain requests or processes making it able to the attacker to execute arbitrary command in vulnerable versions of Bash

6. Once you've run the exploit while listening in the port used in the previous command you'll get a reverse shell, shell you might want to make it more stable with some techniques previously explained

7. Now, going after the root access, the first thing you have to do is run a sudo -l in order to see if you've execute access to a file as the root user

8. In this particular machine we've execute access to PERL so the idea of making a script in PERL to make a shell may come across

9. Now we're only a few steps away from going root, the only thing we've to do is run the following command in the machine's shell: 
	`sudo /usr/bin/perl -e 'exec("/bin/sh -i")'`

>sudo /usr/bin/perl : in order to run perl as su<br>
>-e : to run the program in only one line<br>
>'exec("/bin/sh -i")' : piece of code to execute the bash in interactive mode
