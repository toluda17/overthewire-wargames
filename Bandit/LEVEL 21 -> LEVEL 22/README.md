# Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

# Commands Used
ssh, ls, cat

First, we look at what is in the ‘/etc/cron.d’ folder. Specifically, for this level, I looked at the cronjob ‘cronjob_bandit22’.

```bash
ls -la /etc/cron.d/
```

This cronjob runs the /usr/bin/cronjob_bandit22.sh file as bandit22 user. The five stars indicate it is run every minute, every day. To know what exactly is executed, we need to take a look at the bash file.

```bash
cat /usr/bin/cronjob_bandit22.sh
```

This file creates a file in the ’tmp’ folder and gives read permission to everyone (indicated by the last 4). Then it copies the input of the bandit22 password file into the newly created file.
So the password to the next level is in this created file:

```bash
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

And we get the password!
