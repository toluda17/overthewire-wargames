# Level Goal
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

# Commands Used
ssh, ls, cat

‘.bashrc’ is a file that is run every time a terminal is loaded. This means it is also run when logging in through SSH because this also loads a terminal. Something I have not mentioned is that SSH does not just allows us to log into a machine remotely, but it also allows remote execution of commands by adding the commands after the common SSH expression.
Instead of logging into the machine with SSH, I can execute a command through SSH instead. First, I'll use ls to make sure the readme file is in the folder then use cat to read it:

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 ls
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```

And we obtain the password!
