## Purpose
SMBMap is a useful SMB enumeration tool that enables its users to enumerate samba share drives across an entire domain. It also can list share drives, drive permissions, share contents, upload/download functionality, file name auto-download pattern matching, and even execute remote commands.

## Usage
Default command for a normal usage:
	smbmap -H __{VICTIM's-IP}__ -u __{USER}__ -p __{PASS}__
The following usage is the one you'll have to go with if you want to download a specific file from the server with the usage of a valid User and Password
	smbmap -H __{VICTIM's-IP}__ -u __{USER}__ -p __{PASS}__ --download __{FILE-PATH}__