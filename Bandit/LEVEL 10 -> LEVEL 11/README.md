# Level Goal
The password for the next level is stored in the file data.txt, which contains base64 encoded data

# Commands Used
ls, strings, base64

For this level, we’re required to decode the contents of data.txt, stored in Base64 format, to retrieve the password for the next level. I used the '-d' flag, which decodes files; it tells the base64 command to convert the Base64-encoded text back into its original form:

strings data.txt | base64 -d

