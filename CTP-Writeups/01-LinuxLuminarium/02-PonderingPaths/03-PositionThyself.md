# Position Thyself
This challenge asks us to change our directory before running the program to get the flag.

## My solve
**Flag:** `pwn.college{gnp9f3OtZ5zzn7azY24ktezGjT9.QX2QTN0wSN3AzNzEzW}`

`cd` is a commonly used command that allows you to change your current working directory. 
Syntax: `cd <path/to/directory>`

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /var/log directory.
Please use the `cd` utility to change directory appropriately.

hacker@paths~position-thy-self:~$ cd /var/log

hacker@paths~position-thy-self:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gnp9f3OtZ5zzn7azY24ktezGjT9.QX2QTN0wSN3AzNzEzW}
```

Notice how after running `cd`, your current working directory was updated in the prompt. Earlier it was `~`, now it is `/var/log`.

Extra info:
- Running `cd` without any arguments will take you to `~`, i.e. your home folder.

## What I learned
I learn about the `cd` command and how it works to change your current working directory.

## References 
None