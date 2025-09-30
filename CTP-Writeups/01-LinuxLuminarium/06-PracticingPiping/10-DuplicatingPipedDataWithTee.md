# Duplicating Piped Data With Tee
Pipe the output of `/challenge/pwn` to `/challenge/college`, but also intercept it to see what `pwn` needs from us.

## My solve
**Flag:** `pwn.college{kEa0zLcqt5cBIbnUyIvKY9RrmVq.QXxITO0wSN3AzNzEzW}`

We use `tee` to intercept the output streams between two commands while piping.
Consider the following:
`cmd1 | tee file1 file 2 | cmd2`.
The `stdout` of `cmd1` is fed as to `tee` as `stdin`. Now, this `tee` will write that (`stdin`/`stdout` of `cmd1`) into any number of specified files, AND also to its own `stdout`. We then pipe that into `cmd2`.
With, this we are able see the output of `cmd1`.

```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn_output | /challenge/college 
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.

hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn_output 
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "kEa0zLcq"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret kEa0zLcq | /challenge/college 

Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{kEa0zLcqt5cBIbnUyIvKY9RrmVq.QXxITO0wSN3AzNzEzW}
```

## What I learned
Splitting outputs using `tee`.

## References 
None.