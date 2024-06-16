1. First you've to apply some enumeration with [Nmap](</General Info/Tools/Enumeracion/Nmap.md>)
2. Now that you know the ports open in the machine the next thing is to enumerate some things about the webpage via Whatweb or any other way of enumeration
3. Once you've ended all that you can go inside the webpage and fool around
4. Once you've went through all the sections you'll see the __Security snapshot__ section, this section has a simple IDOR in the url. The thing you've to do is change the number 1, 2, 3, 4,... to 0 and download the file given.
5. Now that you have a .pcap file that belongs to other person you can scan it with [Wireshark](</General Info/Tools/Wireshark.md>) or [TShark](</General Info/Tools/TShark.md>). Once you've done some research of the file you'll come across with some credentials of the FTP protocol to get into Nathan's account.
6. Once you're inside Nathan's account with the IDOR you can do some [Things to enumerate (Machine)](</General Info/Enumeration/Things to enumerate (Machine).md>) and you'll end up finding some SUID capabilities in Python with the usage of the command "getcap -r / 2>/dev/null". Now that you know this you can exploit it by running the following code in the Python Interactive shell.
```
import os
os.setuid(0)
os.system('cat /root/root.txt')

### OR ###

os.setuid(0)
os.system('chmod u+s /bin/bash')
```