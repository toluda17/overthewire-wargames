# Level Goal
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

# Commands Used
ssh, nc, echo, connect

Using ’netcat’, we can create a connection in server mode - which listens for inbound connection. To have netcat send the password, I use echo and pipe it into netcat. The -n flag is to prevent newline characters in the input. Lastly, we let the process run in the background with &.

```bash
echo -n '0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO' | nc -l -p 1234 &
```
Running the setuid binary with port 1234 means it will connect to our netcat server, receive the password inputted through echo and sends back the next password.

```bash
./suconnect 1234
```

And we get the password!
