# Matching Paths With Square Brackets
Starting from your home directory, run `/challenge/run` with a single argument that bracket-globs into the absolute paths to the `file_b`, `file_a`, `file_s`, and `file_h` files

## My solve
**Flag:** `pwn.college{QxWXSGr41R7IjV3dI-CMYPkS3lB.QX0IDO0wSN3AzNzEzW}`

All the wildcard characters we've learnt so far can be used not just for files but for paths as well.
Applying this to paths:

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{QxWXSGr41R7IjV3dI-CMYPkS3lB.QX0IDO0wSN3AzNzEzW}
```

## What I learned
The fact that all wildcard characters can be applied to paths as well.

## References 
None.