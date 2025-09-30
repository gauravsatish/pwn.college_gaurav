# Storing Command Output
Store the output of `/challenge/run` into `PWN` and print it.

## My solve
**Flag:** `pwn.college{UN0lVBN5BYRKWQd-rKrLULwM6th.QX1cDN1wSN3AzNzEzW}`

You can store the output of a command using command substitution.
`VAR=$(COMMAND)`
```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{UN0lVBN5BYRKWQd-rKrLULwM6th.QX1cDN1wSN3AzNzEzW}
```

## What I learned
Command Substitution.

## References 
None.