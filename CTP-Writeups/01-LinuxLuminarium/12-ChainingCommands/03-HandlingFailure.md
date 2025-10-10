# Handling Failure
Chain `/challenge/first-failure` and `/challenge/second` using `||`.

## My solve
**Flag:** `pwn.college{Uujux89itEc1ISGPv5TgIZKf-D9.01M0MDOxwSN3AzNzEzW}`

`||` can also be used to chain commands, but with this one, the second command will run only if the first one fails. This makes it helpful in providing fallback commands.

```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second 
Nice chaining! Flag: pwn.college{Uujux89itEc1ISGPv5TgIZKf-D9.01M0MDOxwSN3AzNzEzW}
```

## What I learned
Chaining commands with `||`.

## References 
None.