# Removing Files
Remove files using `rm`

## My solve
**Flag:** `pwn.college{4I-y-fxLYFEv9jTVhw3mLY28HAy.QX2kDM1wSN3AzNzEzW}`

`rm` deletes the given file.

```bash
hacker@commands~removing-files:~$ ls
delete_me
hacker@commands~removing-files:~$ rm delete_me 
hacker@commands~removing-files:~$ /challenge/check 
Excellent removal. Here is your reward:
pwn.college{4I-y-fxLYFEv9jTVhw3mLY28HAy.QX2kDM1wSN3AzNzEzW}
```

Extra Info:
To remove an empty folder, use `rmdir`.
To recursively delete a folder and its contents, use `rm -r <folder-name>`.
If the files inside are write-protected, you can use `rm -rf <folder-name>`.
## What I learned
the `rm` command.

## References 
None.