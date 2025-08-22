# Level Goal
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

# Commands Used
ls, cat

Linux permissions define read (r), write (w), and execute (x) rights for the owner, group, and others. ls -l shows them as rwxrwxrwx, with - meaning no access. Setuid (s in place of x) lets a file run with its owner’s privilege:

```bash
./bandit20-do ls /etc/bandit_pass
./bandit20-do cat/etc/bandit_pass/bandit20
```

And we obtained the password!
