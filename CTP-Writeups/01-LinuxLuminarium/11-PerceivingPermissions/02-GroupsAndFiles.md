# Groups And Files
Change the group of `/flag` to read the flag.

## My solve
**Flag:** `pwn.college{gy-LwNOJyuqUoAX4ZyvX4mmK37e.QXxcjM1wSN3AzNzEzW}`

We change the group ownership of a file using `chgrp <group> <file>`. We can also find which groups the user id part of using `id`.
With this knowledge, I first check the ownership of the file and the groups I my user is in (since the question was slightly ambiguous). I see that `hacker` is part of the group `hacker`, so I change the group ownership of the file `/flag` to `hacker` with `chgrp`:
```console
hacker@permissions~groups-and-files:~$ ls -l / | grep flag
-r--r-----    1 root root   60 Oct 10 17:36 flag
hacker@permissions~groups-and-files:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{gy-LwNOJyuqUoAX4ZyvX4mmK37e.QXxcjM1wSN3AzNzEzW}
```

## What I learned
Changing group ownership of a file

## References 
None.