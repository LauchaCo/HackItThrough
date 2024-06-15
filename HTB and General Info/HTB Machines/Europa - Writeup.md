1. Enumerate ports

2. Enumerate possible directories and subdomains

3. Now, seeing that the page has https and also has a ssl certificate you can try to enumerate the ssl cert to find possible mails and subdomains not founded

4. Try every way of connecting to the web server: http with ip, https with ip, https with admin-portal.europacorp.htb, http with admin-portal.europacorp.htb, https with europacorp.htb and http with europacorp.htb

5. Now that you should be in the admin portal page you can try a SQLi attack in order to dump all the users and passwords. This attack particularly is a blind SQLi so you'll have to use a python script to make your way to the credentials. The principal modules you've to use in order to make this tool are: urllib3(Using urllib3.disable_warnings() to disable the ssl warnings in order to, later on, create a session and run s.verify = False to unable the session from verifying the certificate), time (to use it for the time-based attack and to make the app sleep()), requests (To make the post requests), signal (This one is imported to make the app execute smth when the script recieves the SIGINT signal), sys (In order to send the execution end codes like 1 for error or interruption or 0 for success), string (To make it easier to create the payload with all the characters needed). Also, you can add pwntools in order to make the script look fancier and more animated.

6. Now that you should have the admin credentials you can go on and login in order to use the tool to create a vpn, this utility is vulnerable because of the use of regex, this can be seen because of the request intercepted by burpsuite, the request has certain fields like "pattern" or "text" that suggest that the app replaces a pattern in a text with some other random text given

7. One of the most common regex replace function in php is preg_replace() so, you can try to vuln the app as a php page and see what happens. This can be done by the usage of the `/e` character at the end of the pattern to change from. This attack can be seen in depth in "https://bitquark.co.uk/blog/2013/07/23/the_unexpected_dangers_of_preg_replace" or "[[Dangers of preg_replace()]]"

8. After exploiting this attack with a simple 'bash tcp reverse shell' you're ready to do some enumeration in order to perform a privilege escalation attack

9. Now that you're in the machine the only thing you've to do is some enumeration explained in [[Own machine enum]]

10. Once you execute the `cat /etc/crontab` command you'll see that the root user runs a simple binary that tell the system to execute a file located in `/var/www/cmd` called `logcleared.sh`. Taking advantadge of this simple script you can create a file there called `logcleared.sh` that makes bash have the SUID permisson.