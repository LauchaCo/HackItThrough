## Que es?
__Kerberos__ is a computer-network authentication protocol that works on the basis of tickets to allow nodes communicating to prove their identity to one another in a secure manner. It's aimed primarily at a client-server model, and it provides mutual authentication - both the user and the server verify each other's identity. Kerberos protocol messages are protected against eavesdropping and replay attacks.

Kerberos builds on symmetric-key and requires a trusted third-party, and optionally may use public-key cryptography durain certain phases of authentication.

Default port: 88 (UDP)

## Principal attacks
The principal kerberos attacks are the ones listed below, the attacks are listed by the privileges levels needed to make them:

Have connectivity with the [[Domain controller (DC)]] 
- [[Kerberos brute-force]]
- [[ASREPRoast Attack]]
- [[Kerberoasting]]
- [[Pass the key]]
- [[Pass the ticket]]
- [[Silver ticket]]
- [[Golden ticket]]
It requires Domain Administrator privileges or similar

## Principal tools for attacking
The principal tools required to attack Kerberos are:

- Impacket examples written in python to carry out Kerberos attacks