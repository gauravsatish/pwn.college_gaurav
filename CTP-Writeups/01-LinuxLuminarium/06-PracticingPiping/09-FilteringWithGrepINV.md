# Challenge Name
Use `-v` to get the flag with `grep`.

## My solve
**Flag:** `pwn.college{AsRniDcYLzmsiVq8uGg1Txu4vZq.0FOxEzNxwSN3AzNzEzW}`

when using the `-v` flag for `grep`, it returns all the lines that does NOT contain the keyword.

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{AsRniDcYLzmsiVq8uGg1Txu4vZq.0FOxEzNxwSN3AzNzEzW}
```

## What I learned
The `-v` flag with `grep`.

## References 
None.