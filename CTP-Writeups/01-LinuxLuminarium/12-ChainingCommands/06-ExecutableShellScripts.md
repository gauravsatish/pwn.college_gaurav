# Executable Shell Scripts
Make a shellscript that will invoke `/challenge/solve`, make it executable, and run it without explicitly invoking `bash`

## My solve
**Flag:** `pwn.college{Qh_dHBPDfNUOUtkIIfSnklv7sBQ.QX0cjM1wSN3AzNzEzW}`

If your script is an executable, then you can directly invoke it without having to call `bash` with its path.

**script.sh**:
```bash
/challenge/solve
```

```
hacker@chaining~executable-shell-scripts:~$ vim script.sh
hacker@chaining~executable-shell-scripts:~$ chmod +x script.sh 
hacker@chaining~executable-shell-scripts:~$ ./script.sh 
Congratulations on your shell script execution! Your flag:
pwn.college{Qh_dHBPDfNUOUtkIIfSnklv7sBQ.QX0cjM1wSN3AzNzEzW}
```

## What I learned
Running scripts directly by making them executables.

## References 
None.