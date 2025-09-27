# Helpful Programs
Append `--help` to a command to read a brief documentation. Do this to the flag program to get the flag.

## My solve
**Flag:** `pwn.college{Eq2j7S6DCPSO7W3qwB-hpihax7q.QX3IDO0wSN3AzNzEzW}`

Self explanatory.

```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 276
hacker@man~helpful-programs:~$ /challenge/challenge -g 276
Correct usage! Your flag: pwn.college{Eq2j7S6DCPSO7W3qwB-hpihax7q.QX3IDO0wSN3AzNzEzW}
```

## What I learned
Use `--help` appended to a command to see a brief overview of its documentation. This can also be `-h` sometimes.

## References 
None.