# Cracking Passwords
Use `John the Ripper` to crack the password with the hash from /etc/shadow leak stored in `/challenge/shadow-leak`

## My solve
**Flag:** `pwn.college{kXsPRBF4lwAUqVeXaYe7EkgiSAA.QX3UDN1wSN3AzNzEzW}`

Passwords are stored in `/etc/shadow` in modern systems. This is in the format of `username:password-hash`. The password hash is the result of hash function which takes in the password and spits out a random hash that is unique to the password. This function is a one way operation, meaning you can go from password to hash, but not from hash to password.
However, if you know the hash, you can still crack the password using tools like John the Ripper. It uses several methods to find the password, but the main method is to use a wordlist and check if the hash of any candidate on that list matches the hash in `/etc/shadow`.
```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak 
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04798g/s 279.4p/s 279.4c/s 279.4C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run 
Congratulations, you have become Zardus! Here is your flag:
pwn.college{kXsPRBF4lwAUqVeXaYe7EkgiSAA.QX3UDN1wSN3AzNzEzW}
zardus@users~cracking-passwords:/home/hacker$ 
```

## What I learned
Cracking passwords with `John the Ripper`.

## References 
None.