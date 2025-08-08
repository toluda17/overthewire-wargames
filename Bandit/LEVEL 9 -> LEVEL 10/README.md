# Level Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

# Commands Used
ls, strings, grep

Because the file was full of binary data, i couldn't simply use cat or find, I had to use the command 'strings', which extracts and prints human-readable text from binary files:

strings data.txt | grep =
