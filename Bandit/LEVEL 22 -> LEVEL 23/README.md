# Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

# Commands Used
ls, cat, echo

We start the same way as level 22:

```bash
ls -la /etc/cron.d/
cat /etc/cron.d/cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
```

Looking at the ‘/usr/bin/cronjob_bandit23.sh’ script, the last line is similar to level 22. This script just introduces variables. The first variable is ‘myname’ and saves the output from the whoami command. Because this script will be run as bandit23, the whoami command will print ‘bandit22’. So the last line tells us that the password from bandit23 will be written into a file in the ‘/tmp’ folder. The filename is created by the line:
```bash
echo I am user $myname | md5sum | cut -d ' ' -f 1.
```

We only need to substitute $myname with bandit22, execute it and the result is the filename.

```bash
echo I am user bandit22 | md5sum | cut -d ' ' -f 1
```

And we've got the password!
