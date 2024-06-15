## Definition
__Nmap__ is a tool used to look for open ports in a given host. The main extra feature that makes nmap so versatile is that it can use lots of nse scripts that make you able to obtain a lot of useful info

## Usage
Basic usage for full velocity scan:
	nmap -p- __{REMOTE-IP}__ --min-rate=5000 -sS -oG allports -vvv -n -Pn
Detailed port scan:
	nmap -p __{PORTS}__ __{REMOTE-IP}__ -sCV -oN targeted
Scan in look for vulnerabilities that are not contemplated in the -sC flag:
	nmap -p __{PORT}__ __{REMOTE-IP}__ --scripts "vuln and safe"
Get more info about a web page:
	nmap -p __{PORT}__ __{REMOTE-IP}__ --script http-enum