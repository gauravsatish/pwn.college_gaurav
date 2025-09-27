# Exclusionary Globbing.
Use a `[!]` to match all files that don't start with `p`, `w`, or `n`.

## My solve
**Flag:** `pwn.college{4_5kgqi2EGaS52xeNCP1bi385SC.QX2IDO0wSN3AzNzEzW}`

`[!]` - Matches any character that isn't in the brackets.

```bash
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{4_5kgqi2EGaS52xeNCP1bi385SC.QX2IDO0wSN3AzNzEzW}
```

## What I learned
The use of `[!]` wildcard to match files.

## References 
None.