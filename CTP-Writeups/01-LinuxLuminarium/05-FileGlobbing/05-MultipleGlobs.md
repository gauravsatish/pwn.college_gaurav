# Multiple Globs
Use multiple globs to match every file that has the letter p.

## My solve
**Flag:** `pwn.college{wAsoxh9_u6Zen4KcYiKxzqAFfnj.0lM3kjNxwSN3AzNzEzW}`

You can use multiple wildcard characters while globbing.
Therefore:

```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files/
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{wAsoxh9_u6Zen4KcYiKxzqAFfnj.0lM3kjNxwSN3AzNzEzW}
```

## What I learned
Multiple globs are valid.

## References 
None.