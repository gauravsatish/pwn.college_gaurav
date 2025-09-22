# Intro To Commands
This challenge introduces us to commands and asks us to invoke our first command.

## My solve
**Flag:** `pwn.college{gNXpjemC2JuwZRpLBx1WMeuq0-_.QX3YjM1wSN3AzNzEzW}`

We execute `whoami` first, which returns the name of our user on the system.
The standard "syntax" for a terminal prompt (in bash) is:
`<username>@<hostname>:-$
Here,
- `username` - name of our user (in this case `hacker`)
- `hostname` - name of the host machine (in this case it is the name of the challenge, as seen while solving the challenge using ssh)
- `$` - This means that we are logged in as a regular user. There is another option which is `#`, which signifies that we are logged in as a root user. I presume we will learn this later on.

```bash
hacker@hello~intro-to-commands:~$ whoami
hacker
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{gNXpjemC2JuwZRpLBx1WMeuq0-_.QX3YjM1wSN3AzNzEzW}
```

## What I learned
I learnt about the basics of commands in linux, and how to invoke them. I was also shown a standard Linux command `whoami`, which returns the name our user.

## References 
None