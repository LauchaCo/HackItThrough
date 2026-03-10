## Way to use it
The way to use GoBuster for directory listing is: `gobuster dir --wordlist {wordlist} -u {url} -t 200 -k`<br>-k : disables certificate checks<br>The way to use GoBuster for subdomain listing is: `gobuster vhost --wordlist {wordlist} -u {url}`


## Useful flags
`--exclude-length {value}` : Exclude responses with the length equal to value
`-k` : Disables certificate checks

