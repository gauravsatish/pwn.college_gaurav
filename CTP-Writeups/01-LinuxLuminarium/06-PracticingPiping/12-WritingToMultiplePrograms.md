# Writing To Multiple Programs
In this challenge, we have `/challenge/hack`, `/challenge/the`, and `/challenge/planet`. Run the `/challenge/hack` command, and duplicate its output as input to both the `/challenge/the` and the `/challenge/planet` commands!

## My solve
**Flag:** `pwn.college{4QAzb1L7ayMg1DKs2ypljInZ6R7.QXwgDN1wSN3AzNzEzW}`

`>(command)` is used when you want another command to write its output as input to your command, but your command normally accepts only files.


```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
11084150361800624660
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{4QAzb1L7ayMg1DKs2ypljInZ6R7.QXwgDN1wSN3AzNzEzW}
```

## What I learned
The usage of `>(command)`.

## References 
None.