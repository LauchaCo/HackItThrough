## Purpose

## Usages 
Connect to SMB share\
`smbclient //{VICTIM's-IP}/C$ -U {DOMAIN}/user%Password`\
Connect to SMB share via NTLM Hash\
`smbclient //{VICTIM's-IP}/transfer -U user --pw-nt-hash {HASH} -W {DOMAIN}`


#TODO