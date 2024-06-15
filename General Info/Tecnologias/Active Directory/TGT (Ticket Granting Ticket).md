## Definition
A TGT is a file created by the [[Key Distribution Center (KDC)]] portion of the [[Kerberos]] authentication protocol. They are used to grant users access to network resources.
TGT files provide secure data protection once the user and server authenticate them. Once a user is authenticated and has the TGT, they can use it to obtain a [[TGS (Ticket Granting Service)]]. It is then that they are granted access to the resources being protected.

TGT files are encrypted and include a session key (and its expiration date) as well as a user's IP address.