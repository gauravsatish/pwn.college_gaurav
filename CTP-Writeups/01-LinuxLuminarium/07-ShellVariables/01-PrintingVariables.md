# Printing Variables
Print the flag stored in `FLAG`.

## My solve
**Flag:** `pwn.college{w4I88FQS3DshfutkHco5F7uT8mV.QX3UTN0wSN3AzNzEzW}`

You can print variables names using echo, but you must prepend the var with `$` so that the shell knows you are referring to the variable `FLAG` and not a string "FLAG", and this process is called variable expansion.

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{w4I88FQS3DshfutkHco5F7uT8mV.QX3UTN0wSN3AzNzEzW}
```

## What I learned
Shell variables and printing them out.

## References 
None.