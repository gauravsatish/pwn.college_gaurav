# Other Users With su
Switch to the `zardus` user with the password `dont-hack-me` then run `/challenge/run`.

## My solve
**Flag:** `pwn.college{Q5WoUQZ5_ynPz5FtzO597Xkat9Y.QX2UDN1wSN3AzNzEzW}`

You can also specify another user to `su` to switch to that user.

```bash
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run 
Congratulations, you have become Zardus! Here is your flag:
pwn.college{Q5WoUQZ5_ynPz5FtzO597Xkat9Y.QX2UDN1wSN3AzNzEzW}
```

## What I learned
Switching to another user with `su`.

## References 
None.