## Definition

## Usage
The way to use Wfuzz to list subdomains is:
`wfuzz -c --hc=404 -t 200 -w {wordlist} -H "Host:FUZZ.smth.com" {URL}`
Way to use Wfuzz to find some files in a page:
`wfuzz -c --hc=404 -t 200 -w {wordlist} -z list,php-html http://{URL}/FUZZ.FUZ2Z`

## Useful flags
`--hh={int}`  - Used to only list the responses that have a different amount of characters from the one specified
`--hc={int}` - Used to only list the responses that don't have the code specified
`-c` - Used in order to output with colors
`-t {int}` - Used to specify the threads to use in the process
`-w {wordlist}` - Used to specify the wordlist to use
`-z {type,parameters,encoder}` - Used to specify a payload for each FUZZ keyword used in the form of type,parameters,encoder. ex.: `-z list,php-html,{encoder}`
