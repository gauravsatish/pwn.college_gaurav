# Suspending Processes.
Run `/challenge/run`, suspend it, and run it again to get the flag.

## My solve
**Flag:** `pwn.college{w3hpSrBf3aEW9opic62qfGc7WlI.QX1QDO0wSN3AzNzEzW}`

You can suspend processes and send it to the background using `Ctrl + Z`. When this happens, the process remains in memory, but it stops executing all instructions and waits for a resume signal. 

Extra Info:
When you suspend the process, you actually send a `SIGTSTP` signal to the process. The resume signal is `SIGCONT`.
You can view suspended processes with `jobs`

```
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 09:53 pts/0    00:00:00 bash /challenge/run
root         140     138  0 09:53 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 09:53 pts/0    00:00:00 bash /challenge/run
root         145     129  0 09:53 pts/0    00:00:00 bash /challenge/run
root         147     145  0 09:53 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{w3hpSrBf3aEW9opic62qfGc7WlI.QX1QDO0wSN3AzNzEzW}
```

## What I learned
Suspending processes.

## References 
https://en.wikipedia.org/wiki/Job_control_(Unix)#Signals