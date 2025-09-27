# Moving Files
Move the `/flag` file into `/tmp/hack-the-planet` and run `/challenge/check` to get the flag.

## My solve
**Flag:** `pwn.college{45Ri05vFStrEDaWo6jOumA-afQy.0VOxEzNxwSN3AzNzEzW}`

`mv` is used to move files. General syntax:
`mv <file> <destination-folder>`

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check 
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{45Ri05vFStrEDaWo6jOumA-afQy.0VOxEzNxwSN3AzNzEzW}
```

Note:
In this challenge, `mv` has been aliased to a custom program which provides messages for correct or incorrect usage before actually moving the file.

Extra Info:
To rename a file in Linux, we can use the mv command:
`mv <original-name> <new-name>`

## What I learned
The `mv` command.

## References 
None.