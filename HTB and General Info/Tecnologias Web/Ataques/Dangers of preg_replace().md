## Function
Perform a regular expression search and replace

## Dangers
This function has a dangerous property which can lead to code execution in some circumstances. Vulnerable code example:
```
<?php
$in = 'Somewhere, something incredible is waiting to be known';
echo preg_replace($_GET['replace'], $_GET['with'], $in);
?>
```
The code will take a user-supplied regular expression and replace whatever it matches with a user-supplied string. So if we were to call `preg_replace.php?replace=/Known/i&with=eaten`, the script would perform a case-insensitive regex search (the i modifier) and echo Somewhere, something incredible is waiting to be eaten.
Just like in the previous example we used the i modifier to make the script case-insenstive we can also use the modifier 'e' to make the app run the code passed as a php script.

Taking into account the previously seen code, the way to exploit this vulnerability is: 
- Give the app the value to the option to replace a word contained in the original text, followed by '/e'.
- Give in the with field a php code like `system('whoami')`

Another code example could be:
```
<?php
$in = 'Somewhere, something incredible is waiting to be known';
echo preg_replace('/' . $_GET['replace'] . '/i', $_GET['with'], $in);
?>
```
This code has a security measure that gives the illusion to make the script 100% safe, however, the code is far from safe because of the way preg_replace() handles the null bytes. This concept makes the app have some security flaws because the hacker can simply make the previously listed attack and add a null-byte (%00) at the end of the line in order to make the app don't append the final '/i'