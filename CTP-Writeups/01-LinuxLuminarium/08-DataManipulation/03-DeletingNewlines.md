# Deleting New Lines
Delete newline characters from the output of `/challenge/run` to get the flag.

## My solve
**Flag:** `pwn.college{8si7WApOrwmOHg8HVFqifPnG-Bh.0VNxEzNxwSN3AzNzEzW}`

Newline characters are special characters and can only be represented using `\n`. Here, `\` is a escape character and can be used in combination with other characters to denote special characters.
These must be enclosed in quotes otherwise the shell may treat them as something else such as line continuation `\`s (explained in extra info).

Therefore, using the same method as in the previous challenge:
```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{8si7WApOrwmOHg8HVFqifPnG-Bh.0VNxEzNxwSN3AzNzEzW}hacker@data~deleting-newlines:~$ 
```

#### Extra Info:
There are many other characters that can be denoted with `\` such as:
- `\\` - an actual backslash
- `\$` - to denote an actual `$` instead of interpreting it as variable expansion
- \* - to denote an actual `*` instead of the wildcard character. In fact this is the method for any wildcard character.

Another use of `\` is line continuation, where if you have multiple commands or arguments on a single line and it is becoming too long, you can split them up into separate lines using `\` appended at the end of each line.

## What I learned
Newline characters (escape sequence characters in general), and deleting them with `tr`.

## References 
None.