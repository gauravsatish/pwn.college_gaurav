# Using Sudo
Use `sudo` to read the flag.

## My solve
**Flag:** `pwn.college{c9HkbzjPi5kBjyoTqoNr21EzzcK.QX4UDN1wSN3AzNzEzW}`

`sudo` functions similarly to `su`, where its `SUID` bit is set, which lets it run with root privileges. `sudo` uses different policies to validate the user. In most systems, the user is added to a group `wheel`, and `sudo` checks if the user is part of that group while validating the user.

```bash
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{c9HkbzjPi5kBjyoTqoNr21EzzcK.QX4UDN1wSN3AzNzEzW}
```

## What I learned
Using `sudo`.

## References 
None.