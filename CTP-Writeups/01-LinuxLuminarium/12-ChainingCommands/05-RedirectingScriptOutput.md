# Redirecting Script Output
Create a script that calls the `/challenge/pwn` command followed by the `/challenge/college` command, and pipe the output of the script into a single invocation of the `/challenge/solve` command

## My solve
**Flag:** `pwn.college{oZv_PwXYJSKMWr5uq00enZOuV3H.QX4ETO0wSN3AzNzEzW}`

As far as the shell is concerned, out shell script is just another command, and can be treated as such. This means all the redirection methods work with scripts.
**x.sh**:
```bash
/challenge/pwn
/challenge/college
```


```bash
hacker@chaining~redirecting-script-output:~$ vim x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve 
Correct! Here is your flag:
pwn.college{oZv_PwXYJSKMWr5uq00enZOuV3H.QX4ETO0wSN3AzNzEzW}
```

## What I learned
Redirecting script output.

## References 
None.