# Home Sweet Home
Run the program with an argument containing an absolute path to the home directory while still viable under 3 constraints.

## My solve
**Flag:** `pwn.college{QZ2rr2nn9GU7eh5_TyaSmwGx6Pp.QXzMDO0wSN3AzNzEzW}`

**Home Directory**: The folder where all user files are stored. Home directories are stored in `/home`, with each user getting a separate folder. For example, for a user `hacker`, the home folder would be `/home/hacker`.
A common shorthand provided by bash for this is `~`, which expands to `/home/<user>`.

This challenge asks us to provide an argument to the program. The argument is a path that the program will copy the flag to. The argument must satisfy the following three constraints:
- Be an absolute path.
- Be in the home folder.
- Be less than three characters long.

```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{QZ2rr2nn9GU7eh5_TyaSmwGx6Pp.QXzMDO0wSN3AzNzEzW}
```

To be in the home directory and fit the length constraint, we are using the `~` shorthand. Doing so leaves us just one character for the file name, which I have named `f`.
## What I learned
Home directories, and the `~` shorthand.

## References 
None.