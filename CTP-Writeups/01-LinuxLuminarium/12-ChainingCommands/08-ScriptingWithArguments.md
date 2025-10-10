# Scripting With Arguments
Write a script at `/home/hacker/solve.sh` that:
1. Takes two arguments
2. Outputs them in REVERSE order (second argument first, then the first argument)

## My solve
**Flag:** `pwn.college{Azc5ylJCgEO2MifvweLTShD0hcX.0VNzMDOxwSN3AzNzEzW}`

Arguments can be accessed with special variables with `$<arg no>`. For example, first arg with `$1`, second with `$2` and so on.
```bash
hacker@chaining~scripting-with-arguments:~$ vim solve.sh
hacker@chaining~scripting-with-arguments:~$ chmod +x solve.sh
hacker@chaining~scripting-with-arguments:~$ /challenge/run 
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{Azc5ylJCgEO2MifvweLTShD0hcX.0VNzMDOxwSN3AzNzEzW}
```

## What I learned
Working with arguments to shell scripts.

## References 
None.