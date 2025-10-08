# Coco Conjecture

After reading the pdf, I opened the netcat connection on my terminal. It gave me a random number and i had to find the number of iterations for that. Also it was mentioned that it had to be consecutively solved 270 times and each answer had to be given within 0.5 sec (iirc). So it became obvious that we had to use a script for this
Luckily, the challenge also came with a helpful description of certain modules we could use to open the netcat connection in python, so based on that I made this script:

```python
from pwn import remote

def get_iter(n):
    iter = 0
    while (n != 1):
        if (n % 2 == 0):
            n = n/2
        else:
            n = 3*n + 1
        iter += 1
	# See [2]
    return iter 

# print(get_iter(867562916433944609)) # used for testing purposes
r = remote('chall_citadel.cryptonitemit.in', '61234')
res = r.recv(timeout=1).decode()
res = res.split("\n")[5] # See [1]

for i in range(270):
    print("ITER", i, "=========")
    if "flag" in res.lower(): 
    # In hindsight there was no need for this as the flag would be given after exactly 270 iterations, but yeah.
        print(res)
        break
    print("RES:", res)
    num = int(res.split(":")[1].strip()) # To isolate the number as an int from the response
    print("NUM:", num)
    iter = get_iter(num)
    print("ITER:", iter)
    r.send("{iter}\n".encode())
    res = r.recv(timeout=1).decode()
    
```

\[1] - Splits the initial response that contains the description of the challenge, etc into separate lines and then takes the 6th element in that list. That element contains the number to calculate for.
\[2] - Whatever I'm doing is slower than the bit shifting and bit operation magic going on in the official write-ups (and after understanding it I'm amazed).

**Flag**: `citadel{k1ryu_c0c0_h4s_4_g0_4t_4n_uns0lv3d_m4th3m4t1cs_pr0bl3m}`