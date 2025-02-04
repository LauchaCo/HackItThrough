In order to make a reverse-shell more stable you'll need to take the follow steps:
1. script /dev/shell -c bash
2. Ctrl + Z
3. stty raw -echo; fg
4. reset term
5. Set $SHELL and $TERM to /bin/bash and xterm respectively
6. You can also see in a personal shell the size of your console with the command "stty size" and apply it to the other terminal with "stty rows __{ROWS}__ columns __{COLUMNS}__"
