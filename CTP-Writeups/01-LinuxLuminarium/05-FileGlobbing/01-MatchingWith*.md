# Matching With *
`cd` to `/challenge` using at max 4 characters.
## My solve
**Flag:** `pwn.college{8qN4DSuDnmSYtC9_PzhKkVPHt6X.QXxIDO0wSN3AzNzEzW}`

`*` - a wildcard character that can match any character as well as any number of characters.
Using this:

```bash
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /c*e
hacker@globbing~matching-with-:/challenge$ /challenge/run 
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8qN4DSuDnmSYtC9_PzhKkVPHt6X.QXxIDO0wSN3AzNzEzW}
```

We could technically use just 3 characters with `cd /c*`, since no other directory matches that apart from `/challenge`
But doing `cd /*e` results in `cd: Too many arguments` because there are multiple matches for that regex, notably `/home`.
## What I learned
Using the `*` wildcard character to match files.

## References 
None.