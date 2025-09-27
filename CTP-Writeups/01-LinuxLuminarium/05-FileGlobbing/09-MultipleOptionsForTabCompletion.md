# Multiple Options For Tab Completion
Use tab completion prompting to find the flag.

## My solve
**Flag:** `pwn.college{0rJCjNX9LYlHQYyF-P2tFNBnFWv.0lN0EzNxwSN3AzNzEzW}`

When there are multiple options for tab completion, `bash` presents you with all of them and prompts you to add more characters to narrow down the option, where as shells like `zsh` cycle through each option by pressing tab.

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter  
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-f
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fl
pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fla
pwncollege-flag      pwncollege-flamingo  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{0rJCjNX9LYlHQYyF-P2tFNBnFWv.0lN0EzNxwSN3AzNzEzW}
```

## What I learned
When there are multiple options, they are presented to you for choosing.

## References 
None.