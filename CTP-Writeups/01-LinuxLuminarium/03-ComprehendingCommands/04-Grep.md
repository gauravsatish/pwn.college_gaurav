# Grepping For A Needle In A Haystack
Find the flag hidden in a big file using the `grep` command.

## My solve
**Flag:** `pwn.college{kCRrRw2Id3Het0k05w7M8vMZUoW.QX3EDO0wSN3AzNzEzW}`

`grep` is a utility that helps us search for strings that match a regular expression in text files.
Syntax: `grep <search-string> <file-to-search>`
```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt 
pwn.college{kCRrRw2Id3Het0k05w7M8vMZUoW.QX3EDO0wSN3AzNzEzW}
```

Extra Info:
`grep` is more commonly used by piping the output of `cat` to `grep`. In this case, the command would be:
`cat /challenge/data.txt | grep pwn.college`

## What I learned
The `grep` utility.

## References 
None.