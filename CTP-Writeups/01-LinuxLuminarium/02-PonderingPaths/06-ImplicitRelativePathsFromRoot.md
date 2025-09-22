# Implicit Relative Paths From Root
Run the program using relative paths from cwd `/`

## My solve
**Flag:** `pwn.college{ECrc4XPVNn404yGPbYIE729ea0k.QX5QTN0wSN3AzNzEzW}`

Relative paths are paths where your current working directory(CWD) matters. Using the same paths from different CWDs will give you different results.

Here, the absolute path of the program is `/challenge/run`. Since we are in the root folder, we do not need to start from root, and can hence do the following:

```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /

hacker@paths~implicit-relative-paths-from-:/$ challenge/run 
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{ECrc4XPVNn404yGPbYIE729ea0k.QX5QTN0wSN3AzNzEzW}
```

## What I learned
The concept of relative paths and their dependence on the current working directory.

## References 
None.