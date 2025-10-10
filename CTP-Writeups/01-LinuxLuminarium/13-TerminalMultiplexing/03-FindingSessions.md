# Finding Sessions
There are three running screen sessions. Search all of them for the flag by attaching and detaching.

## My solve
**Flag:** `pwn.college{Q--egJ4cN2R-hToEF78xUBVSCeZ.01N4IDOxwSN3AzNzEzW}`

We can list all running screen sessions using `screen -ls`. Example output:
```console
hacker@dojo:~$ screen -ls
There are screens on:
        23847.mysession   (Detached)
        23851.goodwork    (Detached)
        23855.morework    (Detached)
3 Sockets in /run/screen/S-hacker.
```
We can reattach to a specific one using `screen -r` and then specifying either the name or the PID of the process.

```console
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        150.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        139.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        144.session_fc7ee00cf5fb2b9e    (Remote or dead)
        147.session_f78526f2ecf3270f    (Remote or dead)
        150.session_85e6ab484461bf59    (Remote or dead)
        144.session_d2f6fdc79a9d21f7    (Detached)
        147.session_ec7883204f3b39cc    (Detached)
        150.session_e4ce64e89e497c76    (Detached)
8 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 144
Remove dead screens with 'screen -wipe'.
[detached from 144.session_d2f6fdc79a9d21f7]
hacker@terminal-multiplexing~finding-sessions:~$ 
```

Inside `144.session_d2f6fdc79a9d21f7`:
```
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{Q--egJ4cN2R-hToEF78xUBVSCeZ.01N4IDOxwSN3AzNzEzW}
pwn.college{Q--egJ4cN2R-hToEF78xUBVSCeZ.01N4IDOxwSN3AzNzEzW}
```

## What I learned
Finding sessions using `screen -ls`

## References 
None.