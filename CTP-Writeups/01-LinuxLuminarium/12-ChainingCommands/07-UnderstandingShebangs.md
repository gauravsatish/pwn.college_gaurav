# Understanding Shebangs
Create a script at `/home/hacker/solve.sh` that has a proper shebang and outputs "hack the planet". Remember to make it executable, then run `/challenge/run` to verify your script works correctly.

## My solve
**Flag:** `pwn.college{0UCGP4KyoGRTQc1np9XkKCRi9UN.0VOzMDOxwSN3AzNzEzW}`

When invoking a program, the kernel reads the first few bytes to see how it must run this. If it encounters the bytes corresponding to `#!`, it understands that this program must be interpreted, and uses the rest of the bytes on that line as the path to the interpreter.
By prepending `#!/bin/bash` at the beginning of our shell script, it is analogous to calling it with `bash script.sh`.

**solve.sh**:
```bash
#!/bin/bash
echo "hack the planet"
```

```
hacker@chaining~understanding-shebangs:~$ vim solve.sh
hacker@chaining~understanding-shebangs:~$ chmod +x solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run 
Testing your script...
Perfect! Your flag:
Flag: pwn.college{0UCGP4KyoGRTQc1np9XkKCRi9UN.0VOzMDOxwSN3AzNzEzW}
```

## What I learned
Shebangs.

## References 
None.