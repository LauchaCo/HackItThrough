## Used in:
[UpDown - Writeup](<HTB Machines/UpDown - Writeup.md>)

## What does it does
The wrapper __phar__ supports the fopen() function in order to give the input the hability to read and write files. This wrapper is particularly useful when you've to reference a compressed file that contains inside of it a php file with a given payload

## Syntax
`phar://{PATH}`