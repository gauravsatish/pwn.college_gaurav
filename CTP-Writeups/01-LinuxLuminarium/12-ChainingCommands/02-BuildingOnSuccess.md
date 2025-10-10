# Building On Success
Chain `/challenge/first-success` and `/challenge/second` using `&&`.

## My solve
**Flag:** `pwn.college{8_rRg5NizQCAMJr1CfP9JbZ8bDI.0lM0MDOxwSN3AzNzEzW}`

`&&` is similar to `;` in the context of chaining commands, except that with `&&`, the second command will not run unless the first command executes successfully (i.e. it returns an exit code 0).
```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second 
Nice chaining! Flag: pwn.college{8_rRg5NizQCAMJr1CfP9JbZ8bDI.0lM0MDOxwSN3AzNzEzW}
```

## What I learned
Chaining commands with `&&`.

## References 
None.