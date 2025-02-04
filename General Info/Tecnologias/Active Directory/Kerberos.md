## Definition
__Kerberos__ is a computer-network authentication protocol that works on the basis of tickets to allow nodes communicating to prove their identity to one another in a secure manner. It's aimed primarily at a client-server model, and it provides mutual authentication - both the user and the server verify each other's identity. Kerberos protocol messages are protected against eavesdropping and replay attacks.

Kerberos builds on symmetric-key and requires a trusted third-party, and optionally may use public-key cryptography durain certain phases of authentication.

Default port: 88 (UDP)

## Principal attacks
The principal kerberos attacks are the ones listed below, the attacks are listed by the privileges levels needed to make them:

Have connectivity with the [Domain controller (DC)](</General Info/Tecnologias/Active Directory/Domain controller (DC).md>)
- [Kerberos brute-force](</General Info/Active Directory/Kerberos brute-force.md>)
- [ASREPRoast Attack](</General Info/Active Directory/ASREPRoast Attack.md>)
- [Kerberoasting](</General Info/Active Directory/Kerberoasting.md>)
- [Pass the key](</General Info/Active Directory/Pass the key.md>)
- [Pass the ticket](</General Info/Active Directory/Pass the ticket.md>)
- [Silver ticket](</General Info/Active Directory/Silver ticket.md>)
- [Golden ticket](</General Info/Active Directory/Golden ticket.md>)
It requires Domain Administrator privileges or similar:
#TODO

## Principal tools for attacking
The principal tools required to attack Kerberos are:

- Impacket examples written in python to carry out Kerberos attacks
