# Switching Windows
A screen session with two windows is set up:
- Window 0
- Window 1
Attach to the session with `screen -r`, then use one of the key combinations above to switch to Window 1.

## My solve
**Flag:** `pwn.college{cr2PWITu5--TavbRpiNVCgNy_hm.0FO4IDOxwSN3AzNzEzW}`

A screen session can have multiple terminal windows. These can be navigated with using shortcuts:
- `Ctrl-A c` - Create a new window
- `Ctrl-A n` - Next window
- `Ctrl-A p` - Previous window
- `Ctrl-A 0` through `Ctrl-A 9` - Jump directly to window 0-9
- `Ctrl-A "` - bring up a selection menu of all of the windows
```bash
screen -r
```

Window 1, navigated using `Ctrl+A 1`:
```
 cat <<MSG
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
MSG
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Welcome to the window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-A 0 to switch to window 0!
> MSG
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows:~$
```


Window 0, navigated using `Ctrl+A 0`:
```
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{cr2PWITu5--TavbRpiNVCgNy_hm.0FO4IDOxwSN3AzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{cr2PWITu5--TavbRpiNVCgNy_hm.0FO4IDOxwSN3AzNzEzW}
hacker@terminal-multiplexing~switching-windows:~$ 
```


## What I learned
Working with different windows in a screen session

## References 
None.