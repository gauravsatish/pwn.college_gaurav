# Help For Builtins
Use `help <builtin>` to find the flag.

## My solve
**Flag:** `pwn.college{sPCnslvo0FqRGMY1tz3FhYvN0UG.QX0ETO0wSN3AzNzEzW}`

"Builtin" programs are ones that are built into the shell directly. I was curious about this and searched it up. These programs are not present as a binary in `/usr/bin` and are implemented directly into your shell (`bash`, `zsh`, `fish`, etc). 
This is seemingly done to avoid excess process creation and because some commands like `cd` (which changes the CWD) affects the shell directly, and will not work with an external process.

If you do:
```bash
$ type cd
cd is a shell builtin
```
This shows that cd is a builtin.

Coming to the challenge, by doing `help challenge` we can find out the condition required to get the flag. Here `challenge` is the builtin.

```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "sPCnslvo".
hacker@man~help-for-builtins:~$ challenge --secret sPCnslvo
Correct! Here is your flag!
pwn.college{sPCnslvo0FqRGMY1tz3FhYvN0UG.QX0ETO0wSN3AzNzEzW}
```

## What I learned
A new concept called builtins, and how to access their documentation.

## References 
Google for the explanation on builtins.