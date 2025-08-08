# Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

* human-readable
* 1033 bytes in size
* not executable

# Command Used
ls, cd, find, cat

Because we're looking for a file with multiple properties, I used find with certain parameters:

find ./ -type f -size 1033c ! -executable

* ./ : tells us what directory to start our search from
* -type : type of file we're looking for
* -size: size of the file (c stands for bytes)
* ! : means NOT; '! -executable' will therefore mean, "not executable"

After I ran the search, I easily located the file, read it in and got the password!
