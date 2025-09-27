# Hidden Files
Find the flag which is contained in a hidden file.

## My solve
**Flag:** `pwn.college{kYJaxqh00u_btfliZ91XGBoezhj.QXwUDO0wSN3AzNzEzW}`

Hidden files are files that start with a `.` 
This is a universal convention in Linux, and `ls` does not list these by default.
To also list these files, we can use the `-a` flag.
```bash
hacker@commands~hidden-files:~$ ls -a /
.   .dockerenv           bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-1099660859865  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cat /.flag-1099660859865 
pwn.college{kYJaxqh00u_btfliZ91XGBoezhj.QXwUDO0wSN3AzNzEzW}
```

## What I learned
The concept of hidden files.

## References 
None.