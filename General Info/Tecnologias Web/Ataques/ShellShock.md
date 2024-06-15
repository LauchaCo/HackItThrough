This vulnerability enables the attacker to gain remote code execution in a web server. The family of this security bugs is only present in Bash. This vulnerability enables the hacker to make a web app to execute bash code through some web servers implementations that use this programming language to make certain requests or processes

The way to exploit this attack is to send a request with a certain header changed to something random and after that the calling to /bin/bash

payload: ``() { :;}; /bin/bash -c "{Command}"`` or ``() { :; }; echo;echo; /bin/bash -c "{Command}"``