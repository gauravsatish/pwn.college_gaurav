# Explicit Relative Paths From Root
Run the program using relative paths while in the root folder.

## My solve
**Flag:** `pwn.college{85hZtqtB_1oLevz47x6z1M-_syv.QXwUTN0wSN3AzNzEzW}`

In relative paths, there are two implicit entries:
- `.` : which points to the same directory/cwd.
- `..` : which points to the parent directory of the cwd.

Here, we are asked to run the program using the above implicit entry.

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run 
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{85hZtqtB_1oLevz47x6z1M-_syv.QXwUTN0wSN3AzNzEzW}
```

## What I learned
The use of `.` and `..` in relative paths.

## References 
None.