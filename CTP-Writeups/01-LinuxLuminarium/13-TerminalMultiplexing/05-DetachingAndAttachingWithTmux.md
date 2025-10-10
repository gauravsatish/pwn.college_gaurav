# Detaching And Attaching With Tmux
1. Launch tmux
2. Detach from it.
3. Run `/challenge/run` (this will send the flag to your detached session!)
4. Reattach to see your prize

## My solve
**Flag:** `pwn.college{MbKYcvoVg9P0aMCIyrsq0cpHzSN.0VO4IDOxwSN3AzNzEzW}`

`tmux` works similarly to `screen` but uses `Ctrl-B` instead of `Ctrl-A`. To detach, we do `Ctrl-B d`.
To list sessions we do `tmux ls`
To reattach to a session: `tmux attach` or `tmux a`.
```console
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run 
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a
[detached (from session 0)]
```

Tmux session:
```console
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{MbKYcvoVg9P0aMCIyrsq0cpHzSN.0VO4IDOxwSN3AzNzEzW}
Congratulations, here is your flag: pwn.college{MbKYcvoVg9P0aMCIyrsq0cpHzSN.0VO4IDOxwSN3AzNzEzW}
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ 
```

## What I learned
Using tmux to attach and detach

## References 
None.