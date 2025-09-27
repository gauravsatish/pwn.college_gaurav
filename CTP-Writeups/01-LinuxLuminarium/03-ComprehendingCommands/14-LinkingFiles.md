# Linking Files
Create a symlink to find the flag

## My solve
**Flag:** `pwn.college{YlzxN4PbebJNqd_SAGmux1208gA.QX5ETN1wSN3AzNzEzW}`

Two types of links:
- Hard links: Multiple addresses that point directly to the same data (like having two apartment addresses for the same building). If you delete one, the data stays accessible through the other.
- Soft links (symlinks): Contain the path to another file (like a forwarding address). If the original file is deleted, the symlink breaks.

Creating symlinks:
Use ln -s source_file link_name to create a symbolic link. The -s flag is essential - without it, you get a hard link. The original file path comes before the link name in the command.

Identifying symlinks:

- Use file filename command - symlinks show as "symbolic link to /path/to/target"
- Use ls -l - symlinks start with 'l' in permissions and show the target  path
- Symlinks work by reading the original file name and accessing that file automatically

```bash
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag 
About to read out the /home/hacker/not-the-flag file!
pwn.college{YlzxN4PbebJNqd_SAGmux1208gA.QX5ETN1wSN3AzNzEzW}
```

## What I learned
The concept of symlinks.

## References 
None.