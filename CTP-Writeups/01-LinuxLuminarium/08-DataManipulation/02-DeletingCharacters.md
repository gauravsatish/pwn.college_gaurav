# Deleting Characters
Run `/challenge/run` and delete the decoy characters `^` and `%` from the output given using `tr` with the `-d` flag.

## My solve
**Flag:** `pwn.college{M5VPYQ6YuKtwTz4RBPgaGZKGm6n.0FNxEzNxwSN3AzNzEzW}`

The same `tr` utility can also be used to delete characters when used with the `-d` flag. 
Using this, we can specify `^` and `%` as the characters to be deleted:
```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{M5VPYQ6YuKtwTz4RBPgaGZKGm6n.0FNxEzNxwSN3AzNzEzW}
```

## What I learned
Using `tr` to delete characters.

## References 
None.