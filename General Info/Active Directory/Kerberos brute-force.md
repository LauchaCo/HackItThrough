## Intro
Because of kerberos being an authentication protocol it's possible to carry out brute-force attacks against itself. The main advantadges of making this attack against a kerberos service are:
- You doesn't need domain account, you just need KDC visibility
- Pre-auth errors don't register as a failed login normal event, that errors register as a pre-auth failure
- Kerberos indicates if the user is correct or not, even though the password written is wrong. This makes you have an adventadge in case you don't know the usernames
- During the attack you can discover multiple users that don't require pre-auth, this accounts are very useful when it comes to trying an [ASREPRoast Attack](</General Info/Active Directory/ASREPRoast Attack.md>)

## Tools
The tools used to exploit the server via this attack is:
- [Kerbrute](</General Info/Tools/Active Directory/Kerbrute.md>)
