# Tab Completion
Use tab completion to read the flag.

## My solve
**Flag:** `pwn.college{8-DHmjcrJlNsRsoz6eAHIrfcxPX.0FN0EzNxwSN3AzNzEzW}`

Tab Completion is much safer than file globbing, because in commands like `rm`, you might be globbing more files than the ones you intended, leading to loss of data. Hence to still keep the time save of globbing without the dangers, we use tab completion.

```bash
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​ 
pwn.college{8-DHmjcrJlNsRsoz6eAHIrfcxPX.0FN0EzNxwSN3AzNzEzW}
```
The above was done using tab completion.

## What I learned
Tab completion and its benefits over file globbing.

## References 
None.