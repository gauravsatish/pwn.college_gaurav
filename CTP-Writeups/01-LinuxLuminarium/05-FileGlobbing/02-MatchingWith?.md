# Matching With ?
Use the `?` wildcard character to cd into `/challenge` while using `?` for c and l, then run `/challenge/run` for the flag.

## My solve
**Flag:** `pwn.college{0XiTwrmvTOLHWnuxa0YfpN5joP-.QXyIDO0wSN3AzNzEzW}`

`?` - A wildcard character that is similar to `*` in that it matches with any character. However, the key difference is it can match only a single character.

Therefore:

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run 
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{0XiTwrmvTOLHWnuxa0YfpN5joP-.QXyIDO0wSN3AzNzEzW}
```

## What I learned
Using the `?` wildcard character to match files.

## References 
None.