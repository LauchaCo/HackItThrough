## Definition
__Dirty Cow__ is a vulnerability of the linux kernel that affected all Linux-based operating system, including Android devices, that used older versions of the Linux kernel created before 2018. It's a local privilege escalation bug that exploits a race condition in the implementation of the copy-on-write mechanism in the kernel's memory-managment subsystem.

## Way of exploitation
The way to exploit this vulnerability is to use searchsploit:
	searchsploit dirty cow
Once you've listed all the exploits you can download one of them like:
	searchsploit -m linux/local/40839.c
After downloading this file you can cat it out and copy the code in order to paste it on the victim's machine in order to, later on, compile it with gcc and run it