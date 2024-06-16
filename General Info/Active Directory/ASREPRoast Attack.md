## Tools
With the [GETNPUsers.py](</General Info/Tools/Active Directory/GETNPUsers.py.md>) script you can do this attack

## What does it does?
Consists in trying to get a [TGT (Ticket Granting Ticket)](</General Info/Tecnologias/Active Directory/TGT (Ticket Granting Ticket).md>) from the server with the usage of the list of users in order to, with some requests, try to get a hash to crack later on in order to obtain a pass 

## Definition
Once you've got a list of users that don't require pre-auth you can send a request AS_REQ on behalf of one of this users and recieve an AS_REP message correctly. This response contains a piece of the message encrypted with the user key that is obtained from his password. Once you have this piece of message you can try to crack it offline to obtain the users credentials

## How could you end up in an ASREP
If you execute a null session attack with [RPCCLient](</General Info/Tools/Active Directory/RPCClient.md>) and you get a list of all the users in the server you can try to do an ASREPRoast attack in order to get a TGT for a specific user.
If you run [Kerbrute](</General Info/Tools/Active Directory/Kerbrute.md>) to get all the users through the port 88 if available and there is a user that doesn't requires pre-auth of Kerberos

## What to do if you can't nail down this attack
If you're unable to recreate this attack you can try to go for another attack using the tool [GetUserSPN.py](</General Info/Tools/Active Directory/GetUserSPN.py.md>)
