# Scripting With Multiple Conditions
write a script at `/home/hacker/solve.sh` that:
- Takes one argument
- If the argument is "hack", output "the planet"
- If the argument is "pwn", output "college"
- If the argument is "learn", output "linux"
- For any other input, output "unknown"

## My solve
**Flag:** `pwn.college{sP0t02LzVxj4ZBkYNh2TM5kon36.0FOzMDOxwSN3AzNzEzW}`

`elif` statements can also be used in shell scripts. They work similar to how elif/else if statements work in various programming languages.

```bash
#!/bin/bash
if [ "$1" == "hack" ]
then
	echo "the planet"
elif [ "$1" == "pwn" ]
then
	echo "college"
elif [ "$1" == "learn" ]
then
	echo "linux"
else
	echo "unknown"
fi
```

```
hacker@chaining~scripting-with-multiple-conditions:~$ vim solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ chmod +x solve.sh 
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run 
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{sP0t02LzVxj4ZBkYNh2TM5kon36.0FOzMDOxwSN3AzNzEzW}
```

## What I learned
Using the `elif` conditional

## References 
None.