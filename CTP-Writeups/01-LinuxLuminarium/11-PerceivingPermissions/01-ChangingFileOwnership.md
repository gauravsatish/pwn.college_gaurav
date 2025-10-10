# Changing File Ownership
Change the owner of the `/flag` file to the `hacker` user, and then read the flag.

## My solve
**Flag:** `pwn.college{8HgdPK_gTeKg4zkKmTC-iuofShN.QXxEjN0wSN3AzNzEzW}`

`chown` is used the change the owner of a file. You can find the owner using `ls -l`. In this case, the first root refers to the user, the second refers to the root group.
```console
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ ls -l / | grep flag
-r--------    1 hacker root   60 Oct 10 17:26 flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{8HgdPK_gTeKg4zkKmTC-iuofShN.QXxEjN0wSN3AzNzEzW}
```

## What I learned
Changing the owner of a file.

## References 
None.