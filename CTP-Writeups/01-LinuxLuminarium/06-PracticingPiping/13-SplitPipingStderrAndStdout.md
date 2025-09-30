# Split Piping Stderr and Stdout
Redirect `stderr` of `/challenge/hack` to `/challenge/the` and `stdout` to `/challenge/planet`.

## My solve
**Flag:** `pwn.college{M3YJ5pOaSt7TsI_6oeYafIFkiBw.QXxQDM2wSN3AzNzEzW}`

`/challenge/hack` will give some output in `stdout` and `stderr`. We can redirect `stderr` directly to `/challenge/the` using `2> >(command)` which writes `stderr` to the temp file for `/challenge/the`.
Then since `stdout` is still remaining, we can just pipe it to `/challenge/planet`.
```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) | /challenge/planet 
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{M3YJ5pOaSt7TsI_6oeYafIFkiBw.QXxQDM2wSN3AzNzEzW}
```

## What I learned
Reinforced `|`, `>(command)`, and `2>`.

## References 
None.