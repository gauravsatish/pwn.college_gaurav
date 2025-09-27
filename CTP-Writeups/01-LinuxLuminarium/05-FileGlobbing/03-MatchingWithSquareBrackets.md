# Matching with []
Change your working directory to `/challenge/files` and run `/challenge/run` with a single argument that bracket-globs into `file_b`, `file_a`, `file_s`, and `file_h`.

## My solve
**Flag:** `pwn.college{w2zRGI4Ca0CB4Ya3w2XPuH9mbpJ.QXzIDO0wSN3AzNzEzW}`

`[]` - A wildcard character where it can only match a single character, and it can only match a character present within the square brackets.
For example, `[abcd]` can match either `a`, `b`, `c`, or `d`.

```bash
hacker@globbing~matching-with-:~$ cd /challenge/files/
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{w2zRGI4Ca0CB4Ya3w2XPuH9mbpJ.QXzIDO0wSN3AzNzEzW}
```

## What I learned
Using the `[]` wildcard character to match files.

## References 
None.