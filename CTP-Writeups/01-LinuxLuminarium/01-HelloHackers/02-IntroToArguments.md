# Intro To Arguments
This challenge explains the concepts of arguments for a command, and asks us to execute the same `hello` command, this time with an argument.

## My solve
**Flag:** `pwn.college{QyvwVCJVi2CbQ8v0HWOF0As5D5f.QX4YjM1wSN3AzNzEzW}`

The general "syntax" for commands is: 
`<command> <arg1> <arg2> <arg3> .... <argn>`
Each argument is separated by a space, and each argument is passed into the command being executed for use internally.
We also learn a new Linux command: `echo`. `echo` is a simple command that returns all the arguments given to it (i.e. "echoes"). Also, if we give multiple arguments to `echo`, it concatenates all of them with a space in between each argument and returns that whole result as output.
By giving the argument `hackers` to `hello` we are able to get the flag.

```bash
hacker@hello~intro-to-arguments:~$ echo Hello!
Hello!
hacker@hello~intro-to-arguments:~$ echo Hello Hackers!
Hello Hackers!
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{QyvwVCJVi2CbQ8v0HWOF0As5D5f.QX4YjM1wSN3AzNzEzW}
```

## What I learned
I learnt about the concept of arguments, and I also learnt another common Linux command `echo`.

## References 
None