## Purpose
The main purpose of Kerbrute is to try to enumerate all the users in the server with the aid of a dictionary, this attack is particularly useful if you want to end up running an __ASREPRoast__ attack later on.
Although, Kerbrute has a lot of other functions like: bruteforce user:pass combos, bruteforce a single user's pass and test a single password against a list of users

## Usage
The main usage is to try to enumerate all the users within the domain:
	kerbrute userenum --dc __{VICTIM's-IP}__ -d __{DOMAIN ex. active.htb}__ __{WORDLIST}__

#TODO