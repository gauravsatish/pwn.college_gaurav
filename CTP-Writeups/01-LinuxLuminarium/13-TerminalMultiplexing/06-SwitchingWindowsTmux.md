# Switching Windows (tmux)
A tmux session with two windows has been created:
- Window 0 has the flag!
- Window 1 has your warm welcome.
## My solve
**Flag:** `pwn.college{A7SsLTCR5HQEEPrHSR7v-i_1DXS.0FM5IDOxwSN3AzNzEzW}`

We can navigate different windows in a tmux session using the following keybinds. They work similarly to screen.
- `Ctrl-B c` - Create a new window
- `Ctrl-B n` - Next window
- `Ctrl-B p` - Previous window
- `Ctrl-B 0` through `Ctrl-B 9` - Jump to window 0-9
- `Ctrl-B w` - See a nice window picker

```console
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux a
[detached (from session challenge_session)]
```
This takes us to window 1:
Window 1:
```console
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Welcome to the tmux window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-B 0 to switch to window 0!
> MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows-tmux:~$ 
```
We can now navigate to window 0 with `Ctrl-b 0`
Window 0:
```console
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{A7SsLTCR5HQEEPrHSR7v-i_1DXS.0FM5IDOxwSN3AzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{A7SsLTCR5HQEEPrHSR7v-i_1DXS.0FM5IDOxwSN3AzNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$ 
```
## What I learned
Working with windows in tmux.

## References 
None.