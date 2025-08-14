# Level Goal
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

# Commands Used
nmap, openssl

First, we need to find open ports between 31000 to 32000 on localhost and check what services are running on them. I used the nmap command:

* nmap -p 31000-32000 localhost

996 out of the 1000 ports refused connection. I then manually tried with each of the five ports and only port 31790 gave a positive response:

* openssl s_client -connect localhost:31790

After that, we input the password we got from the previous level and in return, we receive a private SSH key. So, we create a file (I called it ‘s17.private’) to put the key into and like in Level 14, we need to make sure that the file only has permissions for the user!

