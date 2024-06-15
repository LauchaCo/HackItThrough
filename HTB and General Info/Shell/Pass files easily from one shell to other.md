## Way to do it
The command to make this is:
`base64 -w 0 file | xclip -sel clip` - This command makes the base64 app to disable line wrapping with the `-w 0`  and encode the code of the file, after that, makes xclip copy all the output to your clipboard

## What to do after
After copying the app the next thing to do is:
`echo "{String base64 encoded}" | base64 -d > filename` - This command basically echoes out the string and pass it to the base64 tool to make it decode it and save it in a file
