## Definition
iPython is an interactive shell that adds some additional features to the traditional python shell

## Way of exploitation
The way to exploit this service is by adding a directory called `profile_default` and, inside of it, create another directory called `startup`. Now that you've the basic structure you can create a simple python script that does anything useful inside the startup folder and the program will automatically run it if it's called from the directory prior to `profile_default`. An example of this kind of exploit can be seen in the machine [Share - Writeup](</HTB Machines/WriteUps/Share - Writeup.md>)
