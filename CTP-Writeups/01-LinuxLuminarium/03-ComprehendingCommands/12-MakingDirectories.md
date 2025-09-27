# Making Directories
Create a `/tmp/pwn` directory and make a `college` file in it. Then run the program to get the flag.

## My solve
**Flag:** `pwn.college{kfvUBaepfFo90dkj_oSDYA2KYVV.QXxMDO0wSN3AzNzEzW}`

`mkdir` is used to create new folders/directories.
Syntax:
`mkdir <folder-name>`
```bash
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ /challenge/run 
Success! Here is your flag:
pwn.college{kfvUBaepfFo90dkj_oSDYA2KYVV.QXxMDO0wSN3AzNzEzW}
```

## What I learned
The `mkdir` command.

## References 
None.