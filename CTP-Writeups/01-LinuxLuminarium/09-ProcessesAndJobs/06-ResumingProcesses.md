# Resuming Processes
Suspend `/challenge/run`, then resume it to get the flag.

## My solve
**Flag:** `pwn.college{sApnQFXXXtv2NWJDgcfb9noeiaA.QX2QDO0wSN3AzNzEzW}`

To resume a a suspended job, you can do `fg`. This works for the most recent suspended job. 

Extra info:
If you have multiple jobs suspended and you wish to resume one that isn't the most recent one, you can first do `jobs`, then get the numerical id linked to that suspended job (called the job ID), then do `fg %<num id>`.

```
hacker@processes~resuming-processes:~$ /challenge/run 
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{sApnQFXXXtv2NWJDgcfb9noeiaA.QX2QDO0wSN3AzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## What I learned
Resuming jobs with `fg`.

## References 
Google - for how to resume a specific job
https://en.wikipedia.org/wiki/Job_control_(Unix)#Job_ID