## Usage
Redirect all traffic that arrives a certain port to another machine in a same or different port
```
./socat TCP-LISTEN:{Recieving-Port},fork TCP:{Target-IP}:{Target-Port}
```