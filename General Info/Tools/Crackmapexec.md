## Purpose
Crackmapexec: Can be used to enumerate -> ldap, ftp, winrm, ssh, smb, rdp and mssql

## Usages
List share of a particular user with username and password:
`crackmapexec smb {VICTIM's-IP} -u {USER} -p {PASS} --shares`
List share of a particular user with a NTLM hash
`crackmapexec smb {VICTIM's-IP} -u {USER} -H {NTLM-hash}`
Password spraying:
`crackmapexec smb {VICTIM's-IP} -u usernames.txt -p password --shares`

#TODO