# Hijacking Commands
Find the flag without `/flag` getting deleted.

## My solve
**Flag:** `pwn.college{oWTaHWWsFBj9rx2L_eW7pKeCsg8.QX3cjM1wSN3AzNzEzW}`

Here we have to make sure that the `rm` command encountered by the shell is ours and not the default one. We do this by making that the folder our rm resides in is before the normal one:
```console
hacker@path~hijacking-commands:~$ nvim rm
hacker@path~hijacking-commands:~$ chmod +x rm
hacker@path~hijacking-commands:~$ export PATH="/home/hacker:$PATH"
hacker@path~hijacking-commands:~$ which rm
/home/hacker/rm
hacker@path~hijacking-commands:~$ /challenge/run 
Trying to remove /flag...
Found 'rm' command at /home/hacker/rm. Executing!
pwn.college{oWTaHWWsFBj9rx2L_eW7pKeCsg8.QX3cjM1wSN3AzNzEzW}
```

rm:
```bash
/run/dojo/bin/cat /flag
```

## What I learned
Reinforced previous concepts

## References 
None.