# Level Goal
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

# Command Used
ls, cd, file, cat

After listing all files in the directory:

```bash
* -file00
* -file01
* -file02
* -file03
* -file04
* -file05
* -file06
* -file07
* -file08
* -file09
```

I originally thought I'd have to cat each and every file but then I remembered about the 'file' command. The 'file' command determines and displays the type of each file I give it. After using file, i was presented with:

```bash
* ./-file00: data
* ./-file01: data
* ./-file02: data
* ./-file03: data
* ./-file04: data
* ./-file05: data
* ./-file06: data
* ./-file07: ASCII text
* ./-file08: data
* ./-file09: data
```

As we can see, only file07 contains ASCII text (human readable); from there, it was easy to cat the file and obtain the password.
