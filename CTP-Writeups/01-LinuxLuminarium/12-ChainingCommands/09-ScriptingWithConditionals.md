# Scripting With Conditionals
Write a script at `/home/hacker/solve.sh` that:
- Takes one argument
- If the argument is "pwn", output "college"
- For any other input, output nothing

## My solve
**Flag:** `pwn.college{IA2MXlHpK0tg3tkto6OEz1M3tiu.0lNzMDOxwSN3AzNzEzW}`

This is the general syntax for a conditional in bash:
```bash
if [ "$1" == "ping" ]
then
    echo "pong"
fi
```
This checks if the first argument is "ping", if so it prints "pong".

This is the solution to the challenge:
**solve.sh**:
```bash
#!/bin/bash
if [ "$1" == "pwn" ]
then
	echo "college"
fi
```

```
hacker@chaining~scripting-with-conditionals:~$ vim solve.sh 
hacker@chaining~scripting-with-conditionals:~$ chmod +x solve.sh 
hacker@chaining~scripting-with-conditionals:~$ /challenge/run 
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{IA2MXlHpK0tg3tkto6OEz1M3tiu.0lNzMDOxwSN3AzNzEzW}
```

## What I learned
Conditionals in shell scripts.

## References 
None.