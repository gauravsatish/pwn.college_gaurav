# Detaching And Attaching
For this challenge, you'll need to:
1. Launch screen
2. Detach from it.
3. Run `/challenge/run` (this will secretly send the flag to your detached session!)
4. Reattach to see your prize

## My solve
**Flag:** `pwn.college{0NnVH_6EeCVFdbdUMoSyE4VFPyC.0lN4IDOxwSN3AzNzEzW}`

Detaching and attaching is a big advantage for using `screen`. Imagine that you are working over a remote connection and the connection drops. When that happens the processes currently running on your normal terminal get killed, erasing the work you were doing. When using `screen` if you connection drops, the terminal gets detached, and you can reattach it back and continue your work like nothing happened.
To detach - `Ctrl-A then d`
To reattach - `screen -r`
```
hacker@terminal-multiplexing~launching-screen:~$ screen
[detached from 139.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run 
Found detached screen session: 139.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
```
Inside the screen session:
```
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{0NnVH_6EeCVFdbdUMoSyE4VFPyC.0lN4IDOxwSN3AzNzEzW}
Yes! Flag is: pwn.college{0NnVH_6EeCVFdbdUMoSyE4VFPyC.0lN4IDOxwSN3AzNzEzW}
hacker@terminal-multiplexing~detaching-and-attaching:~$
```

## What I learned
Detaching and reattaching screen sessions.

## References 
None.