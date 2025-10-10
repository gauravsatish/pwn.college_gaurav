# The SUID Bit
Add the SUID bit to `/challenge/getroot`, then read the flag.

## My solve
**Flag:** `pwn.college{UngBoKkxP2JKmr3eCEvLfDaO-s3.QXzEjN0wSN3AzNzEzW}`

The SUID bit is a special bit that appears in the exec position for the user scope in permissions. It means that the program will execute as the user.

It is represented by `s`, and can be added as so:

```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot 
hacker@permissions~the-suid-bit:~$ /challenge/getroot 
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{UngBoKkxP2JKmr3eCEvLfDaO-s3.QXzEjN0wSN3AzNzEzW}
```

## What I learned
Setting the SUID bit

## References 
None.