# The Root
This challenge asks us to invoke a command `pwn` which is stored in `/` using its absolute path.

## My solve
**Flag:** `pwn.college{Mqqw92MTF8uWSDTHJXrlwfJjKkw.QX4cTO0wSN3AzNzEzW}`

Absolute paths are paths where there is a clear starting point, and that path will be valid regardless of your current working directory. In this challenge, we are asked to run a command `pwn` stored in `/` using its absolute path. The filesystem of Linux is designed in such a way that `/` (called the root folder) is the highest up the hierarchy you can go. Every file, folder, everything is under this root folder. With this knowledge, we can start from this root folder and build our path, and with this method our path will be valid everywhere, i.e. an absolute path.

Extra Information:
Another common absolute path is `~`. This signifies your home directory (which I presume we will learn later). As long as you are logged in to your user, `~` is valid. This actually leads to `/home/<user>` where `<user>` is your username.

```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{Mqqw92MTF8uWSDTHJXrlwfJjKkw.QX4cTO0wSN3AzNzEzW}
```

## What I learned
I learnt about absolute paths, and the fact that they are valid everywhere regardless of your current working directory.

## References 
None