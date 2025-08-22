# Level Goal
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new.

# Commands Used
ls, diff

This was a pretty basic level. I simply used the 'diff' command to print out the lines in passwords.new that weren't in passwords.old:

```bash
diff passwords.old passwords.new
```

And we got the password!
