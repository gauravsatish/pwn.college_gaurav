# The PATH Variable
`/challenge/run` will attempt to delete the flag using the `rm` command, make it so that it can't find the `rm` command.

## My solve
**Flag:** `pwn.college{0IZK4aEMHQDjDfWrejyCDIyzN3x.QX2cDM1wSN3AzNzEzW}`

The PATH variable consists of a list of directors that the shell will search for when you enter a command. For example, on my system `ls` is stored in `/usr/sbin` (found using `which ls`). This directory is listed in `PATH`, therefore the shell runs that binary.
```bash
hacker@path~the-path-variable:~$ export PATH=""
hacker@path~the-path-variable:~$ /challenge/run 
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{0IZK4aEMHQDjDfWrejyCDIyzN3x.QX2cDM1wSN3AzNzEzW}
```

## What I learned
PATH variables

## References 
Add any references or videos u used while solving the challenge.