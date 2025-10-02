# Extracting The First Lines With Head
Pipe the output of `/challenge/pwn` to `head` making sure only 7 lines are used, then pipe that to `challenge/college`.

## My solve
**Flag:** `pwn.college{YpocbkzNLzN4B30Qowvp7xPsHW9.0lNxEzNxwSN3AzNzEzW}`

When working with very verbose programs, sometimes you may want to look at only the first few lines of the output of that program. This can be done using `head` which prints only the first 10 lines by default. To specify the exact number of lines needed, use `-n <no-of-lines>`.

Here, the output of `/challenge/pwn` needs to be piped to `head`, and that in turn needs to be piped to `/challenge/college`:
```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college 
Congratulations, you piped the right codes!
pwn.college{YpocbkzNLzN4B30Qowvp7xPsHW9.0lNxEzNxwSN3AzNzEzW}
```

## What I learned
The `head` utility and its arguments and uses.

## References 
None.