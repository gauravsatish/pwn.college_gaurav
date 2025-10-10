# Setting PATH
This level's `/challenge/run` will run the `win` command via its bare name, but this command exists in the `/challenge/more_commands/` directory, which is not initially in the PATH. The `win` command is the _only_ thing that `/challenge/run` needs, so you can just overwrite `PATH` with that one directory.

## My solve
**Flag:** `pwn.college{8_AQUeTmMRNXsSQLT0JGtY1f62A.QX1cjM1wSN3AzNzEzW}`

Here, we have a program `win` stored in `/challenge/more_commands`, we must add this to PATH. This can be done as shown below. Note that this method does not erase the existing contents of PATH, rather appends the folder to it.
```console
hacker@path~setting-path:~$ export PATH="$PATH:/challenge/more_commands"
hacker@path~setting-path:~$ echo $PATH
/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/challenge/more_commands
hacker@path~setting-path:~$ /challenge/run 
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{8_AQUeTmMRNXsSQLT0JGtY1f62A.QX1cjM1wSN3AzNzEzW}
```

## What I learned
Adding folders to PATH.

## References 
None.