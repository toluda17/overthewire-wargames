# Level Goal
The password for the next level is stored in a file called - located in the home directory

# Commands Used
ls, cat

I was a bit lost here; the file was named '-' and whenever I used 'cat -', it treated it like standard input, so rather than giving me the password, it expected me to write something in. I fixed this problem by using 'cat ./-' instead; this told the system that there was a file called '-' in directory '/'
