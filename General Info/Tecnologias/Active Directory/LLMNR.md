## What is LLMNR
__LLMNR__ is a protocol that allows IPv4 and IPv6 hosts to perform name resolution on the same local network without a DNS server or DNS configuration.

When a DNS query fails, the host broadcasts an LLMNR request on the local network to see if any other host can answer.

__LLMNR__ is a successor of NetBIOS. NetBIOS is an older protocol used in Windows networking. NBT-NS is a component of NetBIOS over TCP/IP (NBT) and is responsible for name registration and resolution. Like LLMNR, NBT-NS is a fallback protocol when DNS resolution fails. It allows local name resolution within a LAN.