1 - Enumerate ports

2 - Enumerate web directories with [[GoBuster]]

3 - Now that you haven't found anything interesting try to enumerate subdomains with [[Wfuzz]]

4 - With Wfuzz you will find a subdomain called store, so the final url will be: store.nunchucks.htb

5 - Now, entering the page you will find a newsteller mail textbox that reports the mail given in the same page, this behaviour could be exploited by the usage of a [[SSTI - Server Side Template Injection]].

6 - Try to enter the simple string {{7\*7}} and look the response with the number 49.

7 - Now that you know that this site is vulnerable to [[SSTI - Server Side Template Injection]] you can try to exploit it via Nunjucks, a templating language for javascript and __Node js__. This exploit can be seen in google with a simple search "node js nunjucks ssti"

8 - Once you've compromised the machine and you've gained a rev-shell you now have to do [[Own machine enum]] in order to see if there's something useful

9 - After running the `getcap` command you'll see that the machine has the "cap_setuid+ep" capability in perl, this means that, you can run, with some commands, the perl application with root privileges

10 - When you try to exploit this you'll see that only certain commands are available in perl, this is because of [[AppArmor]], this app is a security module that makes the linux kernel block certain interactions in programs previously specified

11 - Once you've done some research like `perl apparmor bug` or smth like that you'll come across a brillant solution, shebangs

12 - The way to exploit this bug is as simple as creating a file .sh and add a shebang like #!/usr/bin/perl followed by a simple perl reverse shell that you can obtain from Gtfo bins when searching perl and selecting exploit capabilities

13 - Once you've finished the script you only have to run it and there's your root shell