# Becoming Root With su
Use `su` with the root password `hack-the-planet`.

## My solve
**Flag:** `pwn.college{86HaqaalOpsJJyR-t2EZsDVtYgq.QX1UDN1wSN3AzNzEzW}`

`su` and `sudo` are special binaries, which have their `SUID` bit set. This means that they run with the permissions of the owner of the file rather than the user that executes it.
`su` validates the user by asking for the root password before granting access.

```bash
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag 
pwn.college{86HaqaalOpsJJyR-t2EZsDVtYgq.QX1UDN1wSN3AzNzEzW}
```

## What I learned
Elevating permissions using `su`.

## References 
None