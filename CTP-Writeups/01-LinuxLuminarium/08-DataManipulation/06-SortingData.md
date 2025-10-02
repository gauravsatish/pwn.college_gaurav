# Sorting Data
Sort the flags in `/challenge/flags.txt` alphabetically. The last flag will be the correct one.

## My solve
**Flag:** `pwn.college{Q5g486BdNHrZiYy2GTmf8kK1uVz.0FM0MDOxwSN3AzNzEzW}`

The sort command is used to sort through data in a file or in `stdin.
By default it sorts alphabetically, however there are flags to change that:
- `-r`: sorts in reverse order
- `-n`: sorts numerically
- `-u`: removes duplicate lines (unique lines only)
```bash
hacker@data~sorting-data:~$ sort /challenge/flags.txt 
ovm.bnllege{Q5g386BdNHqZiYy2GSle8jK1uVy.0EL0MCNxvRM3AzMzEzW}
ovm.cnlldge{Q5g475AdNHrZiXy1FTme8kK1tVz.0EL0MDOxvSN3AzNzEyV}
ovm.coklegd{Q5f386BdNHrZiYy2GTmf8jK1uVy.0EM0MDOxwSN3AzNzEzV}
ovm.collegd{P5f385BdNGrZiYy1FTme8kK1uVz.0FL0MCOxwRN3AyNzDyV}
ovn.bokkdge{Q5g486BdNHrZiYx1FTlf8kJ1uVz.0EL0MDNxvSN2AzMzEzW}
ovn.boklege{Q5f375BdNHrZhYy2FTmf7kK1uVz.0FL0LCNwwSM2AzMzEyV}
ovn.college{Q5f476BdMHrYiXy2GTmf8kJ1uVz.0FM0MDOxvSN3AzNzEzW}
owm.boklege{Q4g376BdMGrZiYy2GTme8jK0uVy.0FL0MDOwwSN2AyNzDyW}
.........
# shortened for brevity
.........
pwn.college{Q5g486AcNHrZiYy2FSmf8kK0uUz.0FM0MDOxwSN3AzNzEzW}
pwn.college{Q5g486BdMHrZiYy1FTmf8jK1uVy.0FL0MDOxwSM3AzNzDzW}
pwn.college{Q5g486BdNGrZiYx2GTmf7kK1tVz.0EM0MDNxwSN3AzNzEzW}
pwn.college{Q5g486BdNGrZiYy2GTlf8kK1uVy.0FM0MDOxwSN2AzMyEzW}
pwn.college{Q5g486BdNHrZhXy1GTmf7kK0uVz.0EM0MDOwwSN3AzNzEyW}
pwn.college{Q5g486BdNHrZiYy2GTmf8jK1uVz.0FM0MCOxwSN3AzNzDzW}
pwn.college{Q5g486BdNHrZiYy2GTmf8jK1uVz.0FM0MCOxwSN3AzNzEzW}
pwn.college{Q5g486BdNHrZiYy2GTmf8kK1uUz.0FM0LDOxwSN3AzNzEzW}
pwn.college{Q5g486BdNHrZiYy2GTmf8kK1uVz.0FM0MDOxwSN3AzNzEzW}
```

Here the last flag is the correct one.
## What I learned
Sorting through data with `sort`.

## References 
None.