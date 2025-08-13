# Level Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on.

# Commands Used
ssh 

Unlike our other levels, we're not working to get the password immediately here; instead, we're going to ssh into the local user (our machine) but as bandit 14 instead:

* ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220

After we've connected, we simply read in the file path:

* cat /etc/bandit_pass/bandit14

and get the password!
