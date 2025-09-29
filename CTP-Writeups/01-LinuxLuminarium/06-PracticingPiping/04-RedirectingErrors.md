# Redirecting Errors
For `/challenge/run` redirect `stderr` (instructions) to a file `instructions`, and `stdout` to a file `myflag`.


## My solve
**Flag:** `pwn.college{ozcRapwR5CpmdBix7sfiWN0A32V.QX3YTN0wSN3AzNzEzW}`

File descriptors are unsigned integers that act as identifiers for open input/output streams for a process. These can be different for each process, but there are 3 common FDs for all processes:
- `FD 0` - `stdin`
- `FD 1` - `stdout`
- `FD 2` - `stderr`

You can redirect the output in a specific stream to a file by pre-pending the FD before the `>`. For example, to redirect `stderr` of `cmd` to a file `errors`:
```bash
cmd 2> errors
```
You can also append multiple output streams to separate files individually by specifying it again as show in the solve below:

```
hacker@piping~redirecting-errors:~$ /challenge/run 1> myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions 
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{ozcRapwR5CpmdBix7sfiWN0A32V.QX3YTN0wSN3AzNzEzW}
```

Extra Info:
- A process may employ many FDs for various purposes such as network sockets, IPCs (Inter-Process Communication), Event monitoring, etc.
- You can view all the FDs under `/proc/<PID>/fd`. Substitute the PID of your process in `<PID>`.
## What I learned
A new concept of FDs, and how to redirect the output of a certain stream into a certain file. Also how to redirect multiple output streams simultaneously.

## References 
None.