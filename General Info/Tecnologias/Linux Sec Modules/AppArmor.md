## Definition
__AppArmor__ is a security module of the linux's kernel that enables the system administrator to restrict a program capabilities. The way this program works is by profiles usage, this profiles are configured and, lastly, attached to a specific program or multiple programs. This module is similar to [SELinux](</General Info/Tecnologias/Linux Sec Modules/SELinux.md>).

## Way it works
This security module is installed somewhere in the machine and has certain rules for each app, rules that set what the app is denied to do.

## How to look for the app
You can find it by running the following commands:
`cd /`
`find \-name \*apparmor\* 2>/dev/null | grep -vE "exc_criteria|exc_criteria2|..."`