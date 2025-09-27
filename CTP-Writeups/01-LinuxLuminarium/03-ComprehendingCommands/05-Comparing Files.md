# Comparing Files
Find the real flag by using `diff` to compare `/challenge/decoys_only.txt` and `/challenge/decoys_and_real.txt`.

## My solve
**Flag:** `pwn.college{Il6aNpL4aJv1M3jwkbq1sC47Hhm.01MwMDOxwSN3AzNzEzW}

The challenge gives us two files. One with 100 fake flags and another with the same 100 fake flags plus one real flag. I used `diff` to find what's different.
`diff` compares files line by line and shows only the differences. The output uses specific notations:

- `<` indicates content from the first file 
- `>` indicates content from the second file
- `a` means "add" (new lines in second file)
- `c` means "change" (modified lines)
- `d` means "delete" (lines missing from second file)

```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt 
30a31
> pwn.college{Il6aNpL4aJv1M3jwkbq1sC47Hhm.01MwMDOxwSN3AzNzEzW}
```
This means that after line 30 of file 1, there exists an extra line in file 2 which contains the real flag.
## What I learned
The `diff` command.

## References 
Google, for the different diff notations.