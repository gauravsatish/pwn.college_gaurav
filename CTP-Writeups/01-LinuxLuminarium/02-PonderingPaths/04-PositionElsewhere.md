# Position Elsewhere
A repetition of the previous challenge with a different required cwd.

## My solve
**Flag:** `pwn.college{wZ6rOo74E35X1hFwALg9MnWtAHZ.QX3QTN0wSN3AzNzEzW}`

Same as the previous challenge.
```
hacker@paths~position-elsewhere:~$ /challenge/run 
Incorrect...
You are not currently in the /sys directory.
Please use the `cd` utility to change directory appropriately.

hacker@paths~position-elsewhere:~$ cd /sys

hacker@paths~position-elsewhere:/sys$ /challenge/run 
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{wZ6rOo74E35X1hFwALg9MnWtAHZ.QX3QTN0wSN3AzNzEzW}
```

## What I learned
Same as the previous challenge.

## References 
None.