# Level Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

# Commands Used
ls, mkdir, cp, cd, xxd, file, gunzip, bunzip2, tar, cat

This level was certainly a switch-up from previous levels; from the amount of commands used to the complexity of it all. In this level, we started messing around with zip compression commands and reverting hex back to binary. We were asked to create a temporary directory (probably so we don't clutter the home directory):

* mkdir /tmp/1710

After that, we copied data.txt into the temporary directory and moved into that directory:

* cp data.txt /tmp/1710
* cd /tmp/1710

Now remember, data.txt is a hexdump, so we have to convert it from hex back to binary, using the 'xxd -r' command:

* xxd -r data.txt > data1

After that, we use the 'file' command to check what type of file it is. There are different types of compression formats, but for this level, the ones used were 'gzip', 'bzip2', and 'POSIX tar archive'. For each of these, when decompressing, we use their respective commands and formats:

* 'gzip' : gunzip
* 'bzip2' : bunzip2
* 'POSIX tar archive' : tar -xf

Using the file command the first time, I saw that the first compression was 'gzip', so I ran this command:

* gunzip -c data1>data2

From there, we're shown the compression method used each time, and this is repeated until we finally reach a regular ASCII file format; in which we use the 'cat' command to read it and obtain the password!
