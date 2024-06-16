## Definition
A TGT is a file created by the [Key Distribution Center (KDC)](</General Info/Tecnologias/Active Directory/Key Distribution Center (KDC).md>) portion of the [Kerberos](</General Info/Tecnologias/Active Directory/Kerberos.md>) authentication protocol. They are used to grant users access to network resources.
TGT files provide secure data protection once the user and server authenticate them. Once a user is authenticated and has the TGT, they can use it to obtain a [TGS (Ticket Granting Service)](</General Info/Tecnologias/Active Directory/TGS (Ticket Granting Service).md>). It is then that they are granted access to the resources being protected.

TGT files are encrypted and include a session key (and its expiration date) as well as a user's IP address.