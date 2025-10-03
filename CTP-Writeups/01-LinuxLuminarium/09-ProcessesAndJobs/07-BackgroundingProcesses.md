# Backgrounding Processes
Launch `/challenge/run`, then suspend it, then _background_ it with `bg` and launch another copy while the first one is running in the background!

## My solve
**Flag:** `pwn.college{0zh6-sgoUiM7OptHdpuonNAfS-B.QX3QDO0wSN3AzNzEzW}`

If you wish to resume a suspended process without it tying up your terminal, then you can use `bg` to let it keep running in the background.
`bg` also sends a `SIGCONT` signal, the only difference being its not tied to your terminal.

```
hacker@processes~backgrounding-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         153 S+   bash /challenge/run
root         155 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         153 S    bash /challenge/run
root         163 S    sleep 6h
root         164 S+   bash /challenge/run
root         166 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{0zh6-sgoUiM7OptHdpuonNAfS-B.QX3QDO0wSN3AzNzEzW}
```

## What I learned
Resuming suspended processes in the background.

## References 
None.