# Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

# Commands Used
ls, find, cat

This one was a bit different. There were no public files, everything was hidden so I had to use 'ls -a' to list everything. After that, I used the 'find' command with the given parameters:

```bash
find / -type f -user bandit7 -group bandit6 -size 33c
```

After that, it was easy to concatenate (cat) the given file and obtain the password.
