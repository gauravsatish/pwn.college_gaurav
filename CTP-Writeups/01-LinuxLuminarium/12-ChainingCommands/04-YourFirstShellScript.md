# Your First Shell Script
Create a shell script `x.sh` and run `/challenge/pwn` and `/challenge/college` with that script

## My solve
**Flag:** `pwn.college{okaDmjDtHAZ5X7X3n94izgEIKBl.QXxcDO0wSN3AzNzEzW}`

Shell scripts are files that contain a sequence of commands that execute in order. This makes it easy to automate long processes that require many commands.
Note:
Commands can be put into the shell script using `echo <command> >> x.sh`, but I will be using vim henceforth.

**x.sh**:
```bash
/challenge/pwn
/challenge/college
```


```
hacker@chaining~your-first-shell-script:~$ vim x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{okaDmjDtHAZ5X7X3n94izgEIKBl.QXxcDO0wSN3AzNzEzW}
```

## What I learned
Creating shell scripts.

## References 
None.