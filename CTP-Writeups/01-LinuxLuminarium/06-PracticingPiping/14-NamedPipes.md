# Named Pipes
Store output of `/challenge/run` in a FIFO `/tmp/flag_fifo` and then read from it.

## My solve
**Flag:** `pwn.college{cOhJ3AXuRoo3WTre8xjlQjmhXXF.01MzMDOxwSN3AzNzEzW}`

Named pipes (or FIFOs) are persistent pipes, that stick around instead of being temporary like the ones we used in process substitution.
They are created with `mkfifo <name>`.

#### Advantages:
- All handled in memory, nothing stored to disk.
- Data, once read from the FIFO, is removed.
- Provides automatic synchronization, because the fifo will not let you put it or take out data unless both commands to input and take out the data are running.
- Useful for complex data flows.

Terminal 1:
```
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo 
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!
```
Terminal 2:
```
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo 
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{cOhJ3AXuRoo3WTre8xjlQjmhXXF.01MzMDOxwSN3AzNzEzW}
```

Notice how in terminal 1, the command process did not terminate until we read the contents in terminal 2.

## What I learned
FIFOs.

## References 
None.