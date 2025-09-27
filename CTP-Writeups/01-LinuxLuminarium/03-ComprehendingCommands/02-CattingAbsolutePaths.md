# Catting Absolute Paths
The challenge asks us to use the `cat` command with an absolute path.

## My solve
**Flag:** `pwn.college{wi_g1L2krawknJjDDaSjx0CwfwO.QX5ETO0wSN3AzNzEzW}`

The flag is stored in `/flag`, hence by reading the file using `cat /flag` we can get the flag.
```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{wi_g1L2krawknJjDDaSjx0CwfwO.QX5ETO0wSN3AzNzEzW}
```

## What I learned
`cat` with absolute paths.

## References 
None.