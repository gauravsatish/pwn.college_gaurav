# Process Substitution For Input
Run `diff` with the outputs of `/challenge/print_decoys` and `/challenge/print_decoys_and_flag`.

## My solve
**Flag:** `pwn.college{sdtQsnmr42HUfgn9exECRytMTNR.0lNwMDOxwSN3AzNzEzW}`

To do this, we use input process substitution using `<(command)`. The philosophy in Linux is to treat everything like a file, including standard input and output streams. Therefore, when doing `<(command)`, the shell runs that command, and stores its `stdout` into a temporary file whose path it will substitute in that place.

For example, running:
```bash
cat <(echo hi)
```
is the same as
```bash
cat path/to/temp/file
```
which then prints `hi`, as the output of `echo hi` (ie `hi`) was stored in that temp file.

Using this principle:
```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
14a15
> pwn.college{sdtQsnmr42HUfgn9exECRytMTNR.0lNwMDOxwSN3AzNzEzW}
```

## What I learned
Process substitution for input using `<(command)`.

## References 
None.