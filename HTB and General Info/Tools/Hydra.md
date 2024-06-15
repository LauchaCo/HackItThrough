## Usage
__Hydra__ is a tool used by hackers to try to crack different logins, such as: ftp, ssh, http-post, https-post, http-get, telnet, etc. 

## Commands
The __hydra__ tool can be used in different ways depending in the type of attack you want to perform:
http-post-form:
`hydra -L {WORDLIST} -P {WORDLIST} {IP or URL} http-post-form "/{ENDPOINT}:{POST-BODY}:{INCORRECT-LOGIN-MESSAGE}"`

## Parameters
Useful parameters to keep in mind:
- `-l` - Used when you try to specify a particular login username
- `-L` - Used when you want to specify a wordlist of Usernames for a brute-force attack
- `-p` - Just like the user's case, when you use the lowercase p you are telling the app to use the password passed as the parameter value
- `-P` - You can use this parameter when you need to use a wordlist of passwords for the attack
- `-I` - Ignore a restore file if you've run the hydra tool previously and interrupted it for any reason
- `-R` - Restores the previously aborted/crashed session
- `-s {PORT}` - Used when you try to crack a service credentials but the service is running in a port different than the usual one