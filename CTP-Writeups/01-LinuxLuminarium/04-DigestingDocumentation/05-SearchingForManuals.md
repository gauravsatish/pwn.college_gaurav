# Searching For Manuals
Read the man page for `man` to find out how to search for man pages to find the flag.

## My solve
**Flag:** `pwn.college{0h6i_obPHSLP3A8rJPCswRxwZ5w.QX2EDO0wSN3AzNzEzW}`

In the man page for `man`, we see this:
> -k, --apropos
> Approximately equivalent to apropos.  Search the short manual page descriptions for keywords and  display
> any matches.  See apropos(1) for details.
> 
> K, --global-apropos
> Search  for  text in all manual pages.  This is a brute-force search, and is likely to take some time; if you can, you should specify a section to reduce the number of pages that need  to  be  searched. Search terms may be simple strings (the default), or regular expressions if the --regex option is used.

Since `-k` seems to be faster, we might as well try this first.
```bash
hacker@man~searching-for-manuals:~$ man -k challenge
hiobrswxww (1)       - print the flag!
```
This tells us that there exists a man page called `hiobrswxww` which seems to contain within it the keyword `challenge`.
We can now read this man page with `man hiobrswxww`. In the man page, we see:

> --hiobrs NUM
> 	print the flag if NUM is 063

Therefore:
```bash
hacker@man~searching-for-manuals:~$ /challenge/challenge --hiobrs 063
Correct usage! Your flag: pwn.college{0h6i_obPHSLP3A8rJPCswRxwZ5w.QX2EDO0wSN3AzNzEzW}
```

## What I learned
Searching for man pages.

## References 
None.