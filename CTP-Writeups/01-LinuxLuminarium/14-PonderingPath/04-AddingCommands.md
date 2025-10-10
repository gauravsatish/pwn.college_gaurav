# Adding Commands

## My solve
**Flag:** `pwn.college{kwrri1cMMC3adszT-A49DiSNX24.QX2cjM1wSN3AzNzEzW}`

Same as the previous one, we add the folder the commands resides in (without overwriting the original contents of PATH).
```bash
hacker@path~adding-commands:~$ mkdir scripts
hacker@path~adding-commands:~$ nvim scripts/win
hacker@path~adding-commands:~$ export PATH="$PATH:/home/hacker/scripts"
hacker@path~adding-commands:~$ chmod +x scripts/win 
hacker@path~adding-commands:~$ which win
/home/hacker/scripts/win
hacker@path~adding-commands:~$ /challenge/run 
Invoking 'win'....
pwn.college{kwrri1cMMC3adszT-A49DiSNX24.QX2cjM1wSN3AzNzEzW}
```

## What I learned
Adding commands

## References 
None.