1 - Enumerate ports

2 - Try to search for an exploit to get more information about the services

3 - Look at the page and try to find something

4 - Enumerate existing directories with gobuster. Usage: gobuster dir --wordlist __{WORDLIST}__ -u __{URL}__

5 - Once you have the /dev directory you can use wget to download the hype_key file in order to obtain the rsa private key in hex format

6 - Now try to crack the rsa_private_key with ssh2john.py

7 - When seeing that the cracking attempt didn't work out as expected you may try to go another way by enumerating possible vulns in the webpage. This can be done with: nmap --script "vuln and safe" __{IP}__ -p 443 -oN __{FILENAME}__

8 - Once you've run this discovery proccess you'll be able to see that the webpage has the Hearthbleed bug that may be interesting to exploit

9 - Use searchsploit to find the 32745.py script and run it multiple times until you find a piece of code that says $text=__{BASE64-ENCODED-STRING}__

10 - Decode it and use it to decrypt the rsa_private_key in order to check if that's the password of the ssh service or not

11 - Login into the ssh server with the following command: ssh -i __{KEY}__ user@__{IP}__
	-i : Identity file

The identity file is going to be something like this: 

-----BEGIN RSA PRIVATE KEY-----
Proc-Type: 4,ENCRYPTED
DEK-Info: AES-128-CBC,AEB88C140F69BF2074788DE24AE48D46

DbPrO78kegNuk1DAqlAN5jbjXv0PPsog3jdbMFS8iE9p3UOL0lF0xf7PzmrkDa8R
5y/b46+9nEpCMfTPhNuJRcW2U2gJcOFH+9RJDBC5UJMUS1/gjB/7/My00Mwx+aI6
0EI0SbOYUAV1W4EV7m96QsZjrwJvnjVafm6VsKaTPBHpugcASvMqz76W6abRZeXi
Ebw66hjFmAu4AzqcM/kigNRFPYuNiXrXs1w/deLCqCJ+Ea1T8zlas6fcmhM8A+8P
OXBKNe6l17hKaT6wFnp5eXOaUIHvHnvO6ScHVWRrZ70fcpcpimL1w13Tgdd2AiGd
pHLJpYUII5PuO6x+LS8n1r/GWMqSOEimNRD1j/59/4u3ROrTCKeo9DsTRqs2k1SH
QdWwFwaXbYyT1uxAMSl5Hq9OD5HJ8G0R6JI5RvCNUQjwx0FITjjMjnLIpxjvfq+E
p0gD0UcylKm6rCZqacwnSddHW8W3LxJmCxdxW5lt5dPjAkBYRUnl91ESCiD4Z+uC
Ol6jLFD2kaOLfuyee0fYCb7GTqOe7EmMB3fGIwSdW8OC8NWTkwpjc0ELblUa6ulO
t9grSosRTCsZd14OPts4bLspKxMMOsgnKloXvnlPOSwSpWy9Wp6y8XX8+F40rxl5
XqhDUBhyk1C3YPOiDuPOnMXaIpe1dgb0NdD1M9ZQSNULw1DHCGPP4JSSxX7BWdDK
aAnWJvFglA4oFBBVA8uAPMfV2XFQnjwUT5bPLC65tFstoRtTZ1uSruai27kxTnLQ
+wQ87lMadds1GQNeGsKSf8R/rsRKeeKcilDePCjeaLqtqxnhNoFtg0Mxt6r2gb1E
AloQ6jg5Tbj5J7quYXZPylBljNp9GVpinPc3KpHttvgbptfiWEEsZYn5yZPhUr9Q
r08pkOxArXE2dj7eX+bq65635OJ6TqHbAlTQ1Rs9PulrS7K4SLX7nY89/RZ5oSQe
2VWRyTZ1FfngJSsv9+Mfvz341lbzOIWmk7WfEcWcHc16n9V0IbSNALnjThvEcPky
e1BsfSbsf9FguUZkgHAnnfRKkGVG1OVyuwc/LVjmbhZzKwLhaZRNd8HEM86fNojP
09nVjTaYtWUXk0Si1W02wbu1NzL+1Tg9IpNyISFCFYjSqiyG+WU7IwK3YU5kp3CC
dYScz63Q2pQafxfSbuv4CMnNpdirVKEo5nRRfK/iaL3X1R3DxV8eSYFKFL6pqpuX
cY5YZJGAp+JxsnIQ9CFyxIt92frXznsjhlYa8svbVNNfk/9fyX6op24rL2DyESpY
pnsukBCFBkZHWNNyeN7b5GhTVCodHhzHVFehTuBrp+VuPqaqDvMCVe1DZCb4MjAj
Mslf+9xK+TXEL3icmIOBRdPyw6e/JlQlVRlmShFpI8eb/8VsTyJSe+b853zuV2qL
suLaBMxYKm3+zEDIDveKPNaaWZgEcqxylCC/wUyUXlMJ50Nw6JNVMM8LeCii3OEW
l0ln9L1b/NXpHjGa8WHHTjoIilB5qNUyywSeTBF2awRlXH9BrkZG4Fc4gdmW/IzT
RUgZkbMQZNIIfzj1QuilRVBm/F76Y/YMrmnM9k/1xSGIskwCUQ+95CGHJE8MkhD3
-----END RSA PRIVATE KEY-----

12 - The password and the key are the correct ones, although, we don't have a valid user to test the ssh server

13 - Use the deprecated OpenSSH in your favour and enumerate some users until you find the hype user using the script 45939.py from searchsploit

14 - Once you've the user the rsa file and the password you can now enter the ssh service with the following command: ssh -o PubkeyAcceptedKeyTypes=ssh-rsa -i rsa hype@10.10.10.79
	-o PubkeyAcceptedKeyTypes=ssh-rsa is used to provide the server the key type of the rsa file in order to avoid any kind of error in the server

15 - Once you've compromised the machine you could try to use the command sudo -l to list all the files you've access to as root, or , you could also try to run the command uname -a in order to see if the kernel running in the machine is kinda old

16 - Now you know that you're in front of a version that is vulnerable to an exploit called dirty cow. This vulnerable version can be exploited

16.1 - Another way you could also gain root access to the machine is by reading the .bash_history and find if the root has run any rare command
16.1 - By going through this way you will find that the root user once run the command: tmux -S /.devs/dev_sess.
       With this information we can now see that the root user has a session in a terminal saved in a file inside the machine, so, we can exploit this by running the tmux socket file in order to gain root access to the machine