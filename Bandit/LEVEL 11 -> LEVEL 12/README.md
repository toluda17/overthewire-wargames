# Level Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

# Command Used
ls, cat, tr

After listing the file in the directory; I did some research and learnt about the 'tr' command; which is used to tranlate characters. It reads in standard input, performs a transformation (be it translation, deletion or squeezing), then writes the result to standard output. So I ran this command:

```bash
cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
```
and was able to get the password to the next level!
