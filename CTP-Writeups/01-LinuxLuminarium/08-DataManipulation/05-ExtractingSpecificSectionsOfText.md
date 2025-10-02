# Extracting Specific Sections Of Text
Extract the data from the second column of `/challenge/run` using `cut`, then remove all newline characters in that using `tr`.

## My solve
**Flag:** `pwn.college{43G_h2QH02Ua0L95H9TefHG_7at.01NxEzNxwSN3AzNzEzW}`

The `cut` command is used to output data from a specific column.
General syntax:
`cut -d "<delimiter>" -f <column-number>`.
The delimiter is what actually separates the columns, and the column-number is the number of the column you wish to read from.
After using this command, the output you get is still split into many lines, hence you must remove the newline characters as seen in a previous challenge using `tr -d "\n"`.

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run 
4946 p
29062 w
21677 n
........
# shortened for brevity.
........
20954 E
17311 z
8812 W
28524 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{43G_h2QH02Ua0L95H9TefHG_7at.01NxEzNxwSN3AzNzEzW}
```

## What I learned
The `cut` utility and extracting data from a specific column.

## References 
None.