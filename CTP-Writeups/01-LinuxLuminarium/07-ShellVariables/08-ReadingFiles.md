# Reading Files
Read `/challenge/read_me` into the `PWN` environment variable.

## My solve
**Flag:** `pwn.college{wXbJfVPB10hg60LKnxSSg3Ea0wh.QXwIDO0wSN3AzNzEzW}`

The `read` builtin, at it's core reads the contents of `stdin`. These can come from the user (as shown in the previous challenge), or from another source (an example is what we're doing here).
In this case, using `<`, we are feeding the output of `/challenge/read_me` as `stdin` for the `read` builtin, which then stores that into the `PWN` variable.

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me 
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{wXbJfVPB10hg60LKnxSSg3Ea0wh.QXwIDO0wSN3AzNzEzW}
```

## What I learned
Reading Files into a variable.

## References 
None.