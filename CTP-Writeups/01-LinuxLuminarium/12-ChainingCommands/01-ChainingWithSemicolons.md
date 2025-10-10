# Chaining With Semicolons
Chain `/challenge/pwn` and `/challenge/college` using a semicolon.

## My solve
**Flag:** `pwn.college{o5RHkaGstDvJr7RWsUVO5lgegGR.QX1UDO0wSN3AzNzEzW}`

`;` can be used between two separate commands to chain them in a single line:

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college 
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{o5RHkaGstDvJr7RWsUVO5lgegGR.QX1UDO0wSN3AzNzEzW}
```

## What I learned
Chaining commands with `;`

## References 
None.