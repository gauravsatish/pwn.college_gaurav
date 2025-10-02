# Interrupting Processes
Run `/challenge/run`, which will refuse to give the flag until you interrupt it.

## My solve
**Flag:** `pwn.college{Mze_baM2_Am1i5eDBjrnR4rSSNM.QXzQDO0wSN3AzNzEzW}`

When a process is running in your terminal and you wish to stop it, you can use `Ctrl + C` to send an interrupt signal to the process, which in most cases will result in a graceful shutdown of the process.

Here `/challenge/run` will not give the flag until you force it to shutdown using `Ctrl + C`.

```
hacker@processes~interrupting-processes:~$ /challenge/run 
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{Mze_baM2_Am1i5eDBjrnR4rSSNM.QXzQDO0wSN3AzNzEzW}
```

## What I learned
Using `Ctrl+C` to send an interrupt signal to processes.

## References 
None.