## Principal things to have in mind

1. This attack relays in the Domain Controller (DC) having a NTLM hash that is unencryted, to sum up, is insecure by all means.
2. To stop this attack the only thing you've to do is enable kerberos in order to encrypt the hash and make this attack unsuccessful. (Pass from an unencrypted database to an encrypted database)
3. Tool to make this attack work is: __Hashcat__. When you use this app you've to look for output: MD5 or SHA1 (Hashing algorithms) or a long hash