1. IDOR the password reset functionality by requesting a code for our own user and use it to change the password of the admin user (admin@armaxis.htb)
2. After that enter the admin account with the password recently reseted.
3. Once in the admin account dispatch a weapon with a Markdown payload such as:
	- !\[img](file:\///flag.txt)
4. This was done in order to, from our user account, retrieve the base64 of the "image" to decode it into the flag 