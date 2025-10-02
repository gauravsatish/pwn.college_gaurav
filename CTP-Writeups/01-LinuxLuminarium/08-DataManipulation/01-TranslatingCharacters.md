# Translating Characters
`/challenge/run` will print the flag but with the casing swapped. Use `tr` to reverse the casing and get the flag.

## My solve
**Flag:** `pwn.college{EKfU9G3T6G7kL_6qBdPHdKCWYLJ.01MxEzNxwSN3AzNzEzW}`

`tr` is a cli utility that "**tr**anslates" a specified character to another specified character:
`tr A B` - will replace all occurrences of `A` with `B`.
When used with multiple character:
`tr ABC XYZ` - will replace `A` with `X`, `B` with `Y` and `C` with `Z`.


In this challenge, the first obvious thing that comes to mind, is to specify each and every letter 4 separate times, twice in the first argument and again twice in the second argument. However, this is obviously verbose and ugly.
In the `man` page for `tr`, it is specified:
```
CHAR1-CHAR2
    all characters from CHAR1 to CHAR2 in ascending order
```

This makes it nice and easy for us to list the character ranges.
Therefore:
```bash
hacker@data~translating-characters:~$ /challenge/run | tr A-Za-z a-zA-Z
yOUR CASE-SWAPPED FLAG:
pwn.college{EKfU9G3T6G7kL_6qBdPHdKCWYLJ.01MxEzNxwSN3AzNzEzW}
```

## What I learned
Manipulating data through piping with the `tr` utility.

## References 
`man` page for `tr`.