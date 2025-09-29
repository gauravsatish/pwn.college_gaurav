# Redirecting Input
Redirect input of `PWN` file to `/challenge/run` to get the flag.

## My solve
**Flag:** `pwn.college{YcUE4b7aaxUx3vdSBE_EJ_kmDSN.QXwcTN0wSN3AzNzEzW}`

You can redirect input to a command using `<`. Syntax:
`cmd < input`. This is most commonly used to redirect the contents of a file as input to a command.

This challenge asks us to first store `COLLEGE` in `PWN` using output redirection (re: `echo`). Then we feed that file as input into `challenge/run`.

```
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{YcUE4b7aaxUx3vdSBE_EJ_kmDSN.QXwcTN0wSN3AzNzEzW}
```

## What I learned
Redirecting Input using `<`.

## References 
None.