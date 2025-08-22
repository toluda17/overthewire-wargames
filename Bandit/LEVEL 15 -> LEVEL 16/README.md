# Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.
Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

# Commands Used
ssh, openssl, s_client

OpenSSL is a library for secure communication over networks. It implements the Transport Layer Security (TLS) and Secure Sockets Layer (SSL) cryptographic protocols that are, for example, used in HTTPS to secure the web traffic.
'openssl s_client' is the implementation of a simple client that connects to a server using SSL/TLS. 

As the challenge specifies that SSL encryption is required, I use the OpenSSL client to connect to the localhost server. After sending the current level’s password through the secure connection, the server responds with the password for the following level:

```bash
openssl s_client -connect localhost:30001
```
It asks us for the password we previously obtained for access to the new one and once we've put it through, we get the next password!
