# Command History
This challenge asks us to find the flag which is hidden in the command history.

## My solve
**Flag:** `pwn.college{owN0ppR_Ne_UKt2o8sfUS9sM8It.0lNzEzNxwSN3AzNzEzW}`

In Linux, every time you run a command, is saved to a "command history". This history can be accessed by using the up and down arrow.

Some extra information that I know beforehand:
- The commands typed are stored in memory for each terminal session, and when you close the session those commands are written to a file. In bash, this file is `~/.bash_history`.
- When you want to search for a command that's deep in the history, you can use `CTRL + R` and start typing in your command, and it will search for it.

## What I learned
I learnt about a useful feature in Linux terminals, where your commands are stored for easy access.

## References 
None