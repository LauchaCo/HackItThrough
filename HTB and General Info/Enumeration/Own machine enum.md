## Way to do it
How to enum your own machine:
- `hostname -I`  - Shows your current machine ip
- `ip a`  - Shows you all the interfaces running in your pc
- `id`  - Shows all the groups of the user you're currently on, if you've docker group you can do a complex privilege escalation
- `uname -a`  - Its use is to list your current Linux version
- `lsb_release -a `  - Similar to the previous command it lists the Linux distro with some other things
- `sudo -l`  - List all the files you've access to as root
- `find \-perm -4000 2>/dev/null`  - Its use is to, as well as the previous command, find all the files that have SUID privileges
- `cat /etc/crontab`  - You can list all the scheduled tasks of the machines looking for something interesting
- `getcap -r / 2>/dev/null`  - Is used to list capabilities in order to look for privilege escalation
- `pspy` - You can run pspy in order to see all the processes running in the background within defined time intervals
- `grep -r` - To search for a string in all the files's content recursevily
- `ps -eo user,command` - Used to show all the active processes in the machine, particularly useful if you want to make a "home-made" pspy