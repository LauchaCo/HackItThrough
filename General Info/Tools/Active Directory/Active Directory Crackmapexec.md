## Main usages:
The command to enumerate the smb service is as simple as:
	crackmapexec smb __{VICTIM's-IP}__ 
Command to test if some credentials are useful when it comes to the service specified:
	crackmapexec smb __{VICTIM's-IP}__ -u __{USER}__ -p __{PASS}__
Command to enumerate all the shares the user we've pwned have access to:
	crackmapexec smb __{VICTIM's-IP}__ -u __{USER}__ -p __{PASS}__ --shares
	