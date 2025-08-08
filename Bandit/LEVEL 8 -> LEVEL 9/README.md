# Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

# Commands Used
ls, sort, uniq

Since they said the text only appears once, I used the 'uniq -u' command to filter out all text that are unique (appears only once):
sort data.txt | uniq -u
