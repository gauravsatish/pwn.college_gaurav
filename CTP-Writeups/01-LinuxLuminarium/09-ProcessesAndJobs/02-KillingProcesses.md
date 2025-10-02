# Killing Processes
List processes and find `/challenge/dont_run`, and kill it using its `PID`. Then run `/challenge/run`.

## My solve
**Flag:** `pwn.college{YansY8uOtQrhhAcqFQpSKk44Rsy.QXyQDO0wSN3AzNzEzW}`

We first list the processes, and to make it easy, we can filter for `dont_run` using grep. Here, the PID was `136`. With this, we can use `kill <PID>` to kill a process. Then we run `/challenge/run`.

With default behavior, `kill` will send a `SIGTERM` to the process, which will let it shutdown gracefully.
```
hacker@processes~killing-processes:~$ ps aux | grep dont_run
hacker       136  0.0  0.0 231576  3520 ?        Ss   13:53   0:00 /challenge/dont_run
hacker       155  0.0  0.0 230696  2560 pts/0    S+   13:53   0:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run 
Great job! Here is your payment:
pwn.college{YansY8uOtQrhhAcqFQpSKk44Rsy.QXyQDO0wSN3AzNzEzW}
```

## What I learned
Killing processes.

## References 
None.