# Program And Absolute Paths
Following the footsteps of the previous challenge, this program asks us to run a program `run` stored in the `/challenge` directory.

## My solve
**Flag:** `pwn.college{47eIpw0lu-gXI7-NGFsQbypRtZZ.QX1QTN0wSN3AzNzEzW}`

This program is stored in the `/challenge` directory. Using the knowledge gained in the previous challenge, we can start from the root directory and build our way to the path.

```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{47eIpw0lu-gXI7-NGFsQbypRtZZ.QX1QTN0wSN3AzNzEzW}
```

## What I learned
This challenge was an expansion to the previous one, showing me how to run a program stored in a different folder.

## References 
None.