# Redirecting Output
Use output redirection to write the word `PWN` to a file `COLLEGE`.

## My solve
**Flag:** `pwn.college{Adl7LF--Sma6C4yC0wzhH52DmXM.QX0YTN0wSN3AzNzEzW}`

You can redirect the contents of `stdout` to a file using `>`.
The syntax for this is:
`cmd > filename`, where `cmd` is some command that outputs to `stdout`.
It's also important to note that when using `>`, if the file already exists and contains something, redirecting output to that file will wipe the contents of the file and overwrite it.

```bash
$: echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{Adl7LF--Sma6C4yC0wzhH52DmXM.QX0YTN0wSN3AzNzEzW}
```

## What I learned
Redirecting output using `>`.

## References 
None.