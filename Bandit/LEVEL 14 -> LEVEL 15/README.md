# Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

# Commands Used
cat, nc

We know that localhost is the same machine we're on and port 30000 is running a service that will return the next password once we send the current password. In this level, we're going to make use of the 'nc' command. The 'nc' command (short for netcat) is a command that allows us to connect with network services from the command line. Since we've been given the host and port, all we need to do is pipe the password we received from reading in the file path from the previous level to the nc command, and we'll get the new password:

* cat /etc/bandit_path_bandit14 | nc localhost 30000

And we've gotten our password!
