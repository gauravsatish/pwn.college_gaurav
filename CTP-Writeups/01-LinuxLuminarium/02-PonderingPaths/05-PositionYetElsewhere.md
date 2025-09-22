# Position Yet Elsewhere
A repetition of the previous challenge with a different required cwd.

## My solve
**Flag:** `pwn.college{IjA77Nx5eRd-W9ThSWsv6vXDHzO.QX4QTN0wSN3AzNzEzW}`

Same as the previous challenge.
```
hacker@paths~position-yet-elsewhere:~$ /challenge/run 
Incorrect...
You are not currently in the /usr/share/build-essential directory.
Please use the `cd` utility to change directory appropriately.

hacker@paths~position-yet-elsewhere:~$ cd /usr/share/build-essential/

hacker@paths~position-yet-elsewhere:/usr/share/build-essential$ /challenge/run 
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{IjA77Nx5eRd-W9ThSWsv6vXDHzO.QX4QTN0wSN3AzNzEzW}
```

## What I learned
Same as the previous challenge.

## References 
None.