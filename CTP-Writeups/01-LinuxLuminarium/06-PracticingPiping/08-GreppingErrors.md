# Challenge Name
Use `>&` to pipe `stderr` to `grep` to get the flag.

## My solve
**Flag:** `pwn.college{YHgnSpp85TUwfrpctmh3cawmEc_.QX1ATO0wSN3AzNzEzW}`

The `>&` operator lets us redirect the output of an FD to another FD. If we do `2>& 1`, we redirect the output of `stderr` to `stdout`. This is helpful when we need to pipe `stderr` to another command (since piping does not support any other stream than `stdout`).
```
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{YHgnSpp85TUwfrpctmh3cawmEc_.QX1ATO0wSN3AzNzEzW}
```

## What I learned
The `>&` operator and its uses in redirecting an FD to another FD.

## References 
None.