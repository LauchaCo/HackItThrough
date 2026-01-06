### MSSQL
Netexec in this mode shows if a user/password combination enables to pwn a machine. There are two ways to run this command, with local auth and without it. Without the command it's:
```
netexec mssql sequel.htb -u {USER} -p {PASSWORD}
```
With it:
```
netexec mssql sequel.htb -u {USER} -p {PASSWORD} --local-auth
```
