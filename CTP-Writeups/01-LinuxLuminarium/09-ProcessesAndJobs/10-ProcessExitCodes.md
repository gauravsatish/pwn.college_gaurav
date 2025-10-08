# Process Exit Codes
Get the exit code from `/challenge/get-code` and submit it as an argument with `/challenge/submit-code`.

## My solve
**Flag:** `pwn.college{U9PoW1ACBFS4r7QJUt9FINtfXcs.QX5YDO1wSN3AzNzEzW}`

The exit code for the last run program is stored in the `?` env var. We can access this exit code by treating `?` like a normal variable in bash syntax. To read its value, we prepend it with `$`.
```
hacker@processes~process-exit-codes:~$ /challenge/get-code 
Exiting with an error code!
hacker@processes~process-exit-codes:~$ /challenge/submit-code $?
CORRECT! Here is your flag:
pwn.college{U9PoW1ACBFS4r7QJUt9FINtfXcs.QX5YDO1wSN3AzNzEzW}
```

## What I learned
Exit codes, what they are, how to access them.

## References 
None.