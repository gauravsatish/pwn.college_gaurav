# Changing Permissions
Change the permissions of the `/flag` file to read it. The `/flag` file is owned by `root`, and you can't change that, but you can make it readable.

## My solve
**Flag:** `pwn.college{onhFaPYr4H7chpfGFBbbP1VJ5xu.QXzcjM1wSN3AzNzEzW}`

Before we come to interpreting file permissions, the three permission levels are:
- `r` - for reading from the file
- `w` - for modifying the file or creating/deleting it
- `x` - for executing the file

When we do `ls -l`, we can read the permissions. For example, taking my own writeups folder:
```console
$ ls -l
total 16
-rw-r--r-- 1 gaurav gaurav  750 Oct 10 23:03 01-ChangingFileOwnership.md
-rw-r--r-- 1 gaurav gaurav 1010 Oct 10 23:10 02-GroupsAndFiles.md
-rw-r--r-- 1 gaurav gaurav  717 Oct 10 23:13 03-FunWithGroupsNames.md
-rw-r--r-- 1 gaurav gaurav 1017 Oct 10 23:20 04-ChangingPermissions.md
```

we can see that there are 10 characters consecutively at the beginning.
- The first character denotes what type of file it is. For example, `d` denotes a directory, `-` denotes a normal file, `c` denotes a character device (as seen with /dev/fb0 in a previous challenge), etc.
- The next three bytes denote the read, write and execute permissions for the owning user. We can see that the user `gaurav` (me) has read and write permissions here.
- The next three bytes denote read, write and execute perms for the owning group, which is `gaurav` (group, not the user). In this case, only read perms.
- The next three bytes denote read, write and execute perms for any group or user. Here, they get only read perms.

To change permissions, we use `chmod`. It works in two modes, `modify` and `overwrite`.
In `modify` mode, it will retain the original permissions and just change what is specified. The syntax is as such:
`chmod <scope>(+/-)<perms>`
`scope` denotes to which scope these changes should apply to. For the owning user we use `u`, for the group `g`, for others we use `o`, for everyone `a`. You can also use a combination of them, for example `ug`.
`(+/-)` represents whether you want to add or remove those permissions
`<perms>` represents the actual permissions you want to add or remove.

In this challenge, we add the read `r` permission to the "all" scope (`a`)


```bash
hacker@permissions~changing-permissions:~$ ls -l / | grep flag
-r--------    1 root root   60 Oct 10 17:47 flag
hacker@permissions~changing-permissions:~$ chmod a+r /flag
hacker@permissions~changing-permissions:~$ ls -l / | grep flag
-r--r--r--    1 root root   60 Oct 10 17:47 flag
hacker@permissions~changing-permissions:~$ cat /flag 
pwn.college{onhFaPYr4H7chpfGFBbbP1VJ5xu.QXzcjM1wSN3AzNzEzW}
```

## What I learned
Working with file permissions

## References 
None.