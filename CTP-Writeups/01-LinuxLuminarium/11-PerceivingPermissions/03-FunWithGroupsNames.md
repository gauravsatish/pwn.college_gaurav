# Fun With Groups Names
Find the group `hacker` is in, then change file ownership of `/flag` to that group.

## My solve
**Flag:** `pwn.college{o8NTrqAyWOkfG4Qi2HldRN6hCmO.QXycjM1wSN3AzNzEzW}`

We first find the group `hacker` is part of. In this case it's `grp297`, so we change group ownership of `/flag` to `grp297` so that `hacker` can directly read from it.
```
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp297) groups=1000(grp297)
hacker@permissions~fun-with-groups-names:~$ chgrp grp297 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag 
pwn.college{o8NTrqAyWOkfG4Qi2HldRN6hCmO.QXycjM1wSN3AzNzEzW}
```

## What I learned
Finding groups user is in.

## References 
None.