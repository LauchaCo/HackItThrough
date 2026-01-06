## Way to do it

How to enumerate your own machine (Linux):
- `sudo -l` - Look for files to run as root
- `id` - Look at your group and see if it's interesting or has a rare file to exploit
- `find / -group {GROUP} 2>/dev/null` - Look for files owned by the group specified
- `find / -perm -4000 2>/dev/null` - Look for files that have the SUID permission enabled
- `find / -user {USER} 2>/dev/null` - Look for files owned by the user specified
- `crontab -l` - List the crontab for the user running the command
- `cat /etc/crontab` - List all the process that run regularly
- [Processes enumeration](</General Info/Enumeration/Processes enumeration.md>)
- `hostname -I`  - Shows your current machine ip
- `ip a`  - Shows you all the interfaces running in your pc
- `uname -a`  - Its use is to list your current Linux version
- `lsb_release -a `  - Similar to the previous command it lists the Linux distro with some other things
- `getcap -r / 2>/dev/null`  - Is used to list capabilities in order to look for privilege escalation
- `pspy` - You can run pspy in order to see all the processes running in the background within defined time intervals
- `grep -r` - To search for a string in all the files' content recursively
- `ps -eo user,command` - Used to show all the active processes in the machine, particularly useful if you want to make a "home-made" pspy
- `linpeas` - It's a useful script that makes a thorough search for possible paths to escalate privileges on Linux/Unix/MacOS hosts ([Linpeas](https://github.com/peass-ng/PEASS-ng/tree/master/linPEAS)).
- `winpeas` - It's the same case as linpeas but for Windows hosts ([Winpeas](https://github.com/peass-ng/PEASS-ng/tree/master/winPEAS)).
- `cat /etc/resolv.conf` - Shows Nameservers which can forward queries to other subnets.

How to enumerate your own machine (Windows):
- `Get-Content ..\..\..\..\..\..\inetpub\wwwroot\Web.config` - Obtain the configuration file of the IIS hosted in the machine (Microsoft web server)
- `Get-Content ..\..\..\..\..\..\Users\leo\.ssh\id_rsa` - Obtain the private identification file of the user to log into the SSH service
- `whoami`
- `whoami /priv`
- `net user`