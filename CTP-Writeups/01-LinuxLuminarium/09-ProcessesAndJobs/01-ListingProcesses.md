# Listing Processes
List processes and find the one that will give you the flag.

## My solve
**Flag:** `pwn.college{AuplLTwDiwwOAaHPfOMCo32mcsr.QX4MDO0wSN3AzNzEzW}`

Listing processes can be done with the `ps` command. By default it lists only the processes running in the current terminal, however you can change that using arguments.

There are two ways of specifying arguments:
- Standard syntax: Here you can use `-e` to list every process, `-f` for a full format output.
- BSD syntax: Here you can use `a` to list processes of all users, `u` for a user readable output and `x` to list processes that aren't running in the terminal.

Running either of the commands gives you a list of processes along with various information about them such as the user that created the process, PID, % of cpu and memory utilization, tty, CPU time used, and the actual command along with its arguments.

**PID** - A unique identification number given to any process that is used to refer to it, such as when sending process signals like `SIGTERM` and `SIGKILL`.


Here, we listed all the process using `ps aux`. We can see a process running who's command is `/challenge/12786-run-8595` which seems to be the command that will give the flag. Hence:

```
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   08:01   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspac
root           7  0.0  0.0 231708  2560 ?        S    08:01   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    08:01   0:00 /challenge/12786-run-8595
root         135  0.0  0.0   2744  1600 ?        S    08:01   0:00 sleep 6h
hacker       152  0.0  0.0 231576  3520 pts/0    Ss   08:22   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interac
hacker       158  0.0  0.0 231964  4160 pts/0    S+   08:22   0:00 /run/dojo/bin/bash --login
hacker       171  0.5  0.0 231576  3520 pts/1    Ss   13:44   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interac
hacker       177  0.0  0.0 231964  4160 pts/1    S    13:44   0:00 /run/dojo/bin/bash --login
hacker       186  0.0  0.0 233600  3840 pts/1    R+   13:44   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/12786-run-8595
Yahaha, you found me! Here is your flag:
pwn.college{AuplLTwDiwwOAaHPfOMCo32mcsr.QX4MDO0wSN3AzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
^C
```

## What I learned
Processes, how to list them, PIDs.

## References 
None.