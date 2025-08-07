# Level Goal
The password for the next level is stored in a file called –spaces in this filename– located in the home directory

# Commands Used
ls, cat

This one threw me off a bit; I had originally assumed that surrounding the filename in double quotation marks would deal with the spaces in the name but it didn't work.
So I used '--' to signal the end of command-line options so that cat treats the next argument as a filename, even though it begins with double dashes (--), which would normally be interpreted as a flag or option.
