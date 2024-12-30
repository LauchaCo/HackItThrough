1. Enumerate ports

2. Enumerate web directories with [GoBuster](</General Info/Tools/Enumeracion/Gobuster.md>)

3. Now that you haven't found anything interesting try to enumerate subdomains with [Wfuzz](</General Info/Tools/Enumeracion/Wfuzz.md>)

4. With [Wfuzz](</General Info/Tools/Enumeracion/Wfuzz.md>) you will find a subdomain called store, so the final URL will be: store.nunchucks.htb

5. Now, entering the page you will find a news teller mail textbox that reports the mail given in the same page, this behavior could be exploited by the usage of a [SSTI - Server Side Template Injection](</General Info/Tecnologias Web/Ataques/SSTI - Server Side Template Injection.md>).

6. Try to enter the simple string {{7\*7}} and look the response with the number 49.

7. Now that you know that this site is vulnerable to [SSTI - Server Side Template Injection](</General Info/Tecnologias Web/Ataques/SSTI - Server Side Template Injection.md>) you can try to exploit it via Nunjucks, a templating language for JavaScript and __Node js__. This exploit can be seen in google with a simple search "node js Nunjucks SSTI"

8. Once you've compromised the machine and you've gained a rev-shell you now have to do [Things to enumerate (Machine)](</General Info/Enumeration/Things to enumerate (Machine).md>) in order to see if there's something useful

9. After running the `getcap` command you'll see that the machine has the "cap_setuid+ep" capability in Perl, this means that, you can run, with some commands, the Perl application with root privileges

10. When you try to exploit this you'll see that only certain commands are available in Perl, this is because of [AppArmor](</General Info/Tecnologias/Linux Sec Modules/AppArmor.md>), this app is a security module that makes the Linux kernel block certain interactions in programs previously specified

11. Once you've done some research like `perl apparmor bug` or something like that you'll come across a brilliant solution, shebangs.

12. The way to exploit this bug is as simple as creating a file .sh and add a shebang like #!/usr/bin/perl followed by a simple Perl reverse shell that you can obtain from Gtfo bins when searching Perl and selecting exploit capabilities

13. Once you've finished the script you only have to run it and there's your root shell