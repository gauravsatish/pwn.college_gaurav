# Reading Shell Scripts
Read the `/challenge/run` shell script which requires a secret key that's hardcoded into the script.

## My solve
**Flag:** `pwn.college{s_f5Eu_YLvzr5OYYufvoy0vw4rp.0lMwgDOxwSN3AzNzEzW}`

We have to read the contents of `/challenge/run`. We can do this with `cat /challenge/run`:
```bash
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
	echo "CORRECT! Your flag:"
	cat /flag
else
	echo "Read the /challenge/run file to figure out the correct password!"
```
In this, we can see that the secret key required is `hack the PLANET`. Therefore:

```
hacker@chaining~reading-shell-scripts:~$ /challenge/run 
hack the PLANET
CORRECT! Your flag:
pwn.college{s_f5Eu_YLvzr5OYYufvoy0vw4rp.0lMwgDOxwSN3AzNzEzW}
```

## What I learned
Reading scripts.

## References 
None.