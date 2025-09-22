# Implicit Relative Path
Run the program from the `/challenge` directory.

## My solve
**Flag:** `pwn.college{IMlBaZiKjworRKxTcYqqRNS51hD.QXxUTN0wSN3AzNzEzW}`

In this challenge, we are in the `/challenge` directory and we need the run the program located at `/challenge/run`. However, here we cannot type `run` because it will not actually invoke `/challenge/run`. This is a safety measure because if the program name was the same as a commonly used Linux command, you could accidentally execute the one in the CWD. Hence to explicitly run the program in the CWD, we have to do the following:

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge/

hacker@paths~implicit-relative-path:/challenge$ ./run 
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IMlBaZiKjworRKxTcYqqRNS51hD.QXxUTN0wSN3AzNzEzW}
```

## What I learned
An edgecase regarding running programs in the CWD by calling it specifically using `./run`.

## References 
None.