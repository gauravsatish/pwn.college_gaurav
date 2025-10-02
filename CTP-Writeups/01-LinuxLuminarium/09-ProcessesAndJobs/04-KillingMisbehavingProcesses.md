# Killing Misbehaving Processes
Kill the decoy process hogging `/tmp/flag_fifo`, run `/challenge/run` and read the fifo to get the flag.

## My solve
**Flag:** `pwn.college{gI2vOtuPKU67sfkvqRA9zyGnJYu.0FNzMDOxwSN3AzNzEzW}`

There is a decoy process running that is hogging the fifo at `/tmp/flag_fifo` and sending decoy flags into it. We have to find the PID of that process and kill it, then run `/challenge/run` to send the flag through the fifo, after which we can read from the fifo and get the flag.
The reason we are reading the fifo once before running `/challenge/run` is because the decoy process might have sent data through the fifo which would remain in it until we read from it.
```bash
hacker@processes~killing-misbehaving-processes:~$ ps aux | grep decoy
root         139  0.0  0.0   5204  3520 ?        S    14:32   0:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
hacker       142  0.0  0.0  13516  9280 ?        Ss   14:32   0:00 /usr/bin/python /challenge/decoy
hacker       160  0.0  0.0 230696  2560 pts/0    S+   14:33   0:00 grep --color=auto decoy
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo 
pwn.college{Si80rAMRGdaK8WFqcOM31z4SC9-m0Iue6FaEpKVPV7XUg0A}
pwn.college{.MT26Fr63WJiVU.z-Ec7ACNutweRBniBRmTLN0h99AJRHUl}
pwn.college{I6ti4fYSDb9MO.xFPJag7nDy6nrhCpQgUiCR5.vEUNrGLoF}
pwn.college{dH6wMWWMiz75pQy.a9s7RBckrYMPVtVHQMrUsaJJJ3ZHAAY}
..........
# shortened for brevity
..........
pwn.college{TYi0SySDkXiPbPBYyQ5-evfjLZQc51CAnQ1tTeVU4F4hYq8}
pwn.college{dj1.Ej7yg068ui3u5fxN.N8IbAsSRN0MchjrdOT6kE2UBi5}
pwn.college{1MyeBASxlE9hXIJ7LPexrTd7kKa3SNxGwjg-keAkRa6J6Rv}
pwn.college{VKx0A32MyrH5.400IAUtF0290ZM7JUl5mrSsitzuD1WVi6Z}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run 
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo 
pwn.college{gI2vOtuPKU67sfkvqRA9zyGnJYu.0FNzMDOxwSN3AzNzEzW}
^C
```

## What I learned
Reinforced searching for and killing processes.

## References 
None.