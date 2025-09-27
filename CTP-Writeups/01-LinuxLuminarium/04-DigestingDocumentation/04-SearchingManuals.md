# Searching Manuals
Search for a way to find the flag in the man page.

## My solve
**Flag:** `pwn.college{UCxWGZZg2xtU05baMI0poL6XQZp.QX1EDO0wSN3AzNzEzW}`

By doing `/flag` and pressing `n` in the man page, I found these two lines:
```
       --jnhpf
              This argument will give you the flag!
```

With that:
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --jnhpf
Initializing...
Correct usage! Your flag: pwn.college{UCxWGZZg2xtU05baMI0poL6XQZp.QX1EDO0wSN3AzNzEzW}
```

## What I learned
Searching in man pages.

## References 
None.