# More Catting Practice
Same as previous.

## My solve
**Flag:** `pwn.college{4ul24LUyZebystrHlAPodaLhSv2.QXwITO0wSN3AzNzEzW}`

The flag is stored in `/usr/share/screen/flag`, hence by reading the file using `cat` with an absolute path, we can get the flag.
```bash
hacker@commands~more-catting-practice:~$ cat /usr/share/screen/flag
pwn.college{4ul24LUyZebystrHlAPodaLhSv2.QXwITO0wSN3AzNzEzW}
```

## What I learned
`cat` with absolute paths

## References 
None.