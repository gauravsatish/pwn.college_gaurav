# Scripting With Default Cases
Write a script at `/home/hacker/solve.sh` that:
- Takes one argument
- If the argument is "pwn", output "college"
- For any other input, output "nope"

## My solve
**Flag:** `pwn.college{UaxwifWUld0Wi55MZuBd_2ZZzfQ.01NzMDOxwSN3AzNzEzW}`

The `else` block is run when the condition returns false. It provides a catch for when the main if block doesn't run because the condition fails, or if there are multiple if elif statements it runs if none of them run.

The syntax can be seen in the solve below.
**solve.sh**:
```bash
#!/bin/bash
if [ "$1" == "pwn" ]
then
	echo "college"
else
	echo "nope"
fi
```

```
hacker@chaining~scripting-with-default-cases:~$ vim solve.sh
hacker@chaining~scripting-with-default-cases:~$ chmod +x solve.sh
hacker@chaining~scripting-with-default-cases:~$ /challenge/run 
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{UaxwifWUld0Wi55MZuBd_2ZZzfQ.01NzMDOxwSN3AzNzEzW}
```

## What I learned
Scripting with default cases.

## References 
None.