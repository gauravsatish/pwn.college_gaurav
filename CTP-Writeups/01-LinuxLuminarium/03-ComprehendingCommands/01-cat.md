# Cat: not the pet, but the command!
Read out the contents of the `flag` file in `~` to get the flag.

## My solve
**Flag:** `pwn.college{ELKIIkLFHhX30suUwBbRMTyO2B9.QXxcTN0wSN3AzNzEzW}`

`cat` is a common command in Linux. `cat` is most commonly used for printing the contents of a file to stdout for reading or for piping to other commands.
If given multiple arguments, `cat` will concatenate the contents of all the files and print them.

In this challenge, the flag is in the `~/flag` file. To read it:

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ ls
flag
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{ELKIIkLFHhX30suUwBbRMTyO2B9.QXxcTN0wSN3AzNzEzW}
```

## What I learned
The `cat` utility.

## References 
None.