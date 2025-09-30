# Exporting Variables
Invoke `/challenge/run` with the `PWN` variable exported and set to the value `COLLEGE`, and the `COLLEGE` variable set to the value `PWN` but _not_ exported.

## My solve
**Flag:** `pwn.college{4p97QISx3Xnfn9EnRVyw0QGwppP.QXyYTN0wSN3AzNzEzW}`

When we initialise a variable, that variable is valid only for the current shell. Any new shells created will not have that variable. To solve this issue, we *export* the variable using `export VAR=VALUE`. Then, this variable is accessible in all shells that are subprocesses of our main shell.

```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run 
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{4p97QISx3Xnfn9EnRVyw0QGwppP.QXyYTN0wSN3AzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```
Extra Info:
If we wish to have a global set of variables that are available in every shell regardless of whether they are subprocesses of a main shell or not, we usually define them with `export` in a `.bashrc` or a `.zshrc` file, depending on your shell. This file runs every time you create a shell, and when we define it in that file, every time it runs we get those variables in all the shells.

## What I learned
Exporting variables.

## References 
None.