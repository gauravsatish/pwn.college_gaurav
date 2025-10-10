# Finding Commands
In this challenge, there is a `win` directory somewhere in `$PATH`, but it won't give you the flag. Instead, it's in the same directory as a `flag` file that we made readable by you! You must find `win` (with the `which` command), and `cat` the flag out of that directory

## My solve
**Flag:** `pwn.college{AZc1T0RT9LHq2Ds4PF5gceNTcmJ.01NzEzNxwSN3AzNzEzW}`

`which` is used to print the directory of a program. It goes through all the folders in PATH and returns the first match for the command.
```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/25706/win
hacker@path~finding-commands:~$ cat /challenge/paths/25706/flag
pwn.college{AZc1T0RT9LHq2Ds4PF5gceNTcmJ.01NzEzNxwSN3AzNzEzW}
```

## What I learned
Using `which` to get the directory of a command.

## References 
None.