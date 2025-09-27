# An Epic Filesystem Quest
Follow the clues using `cat`, `ls` and `cd` to find the flag

## My solve
**Flag:** `pwn.college{os8u_uJp4S0st_jFAEk6AX9S72i.QX5IDO0wSN3AzNzEzW}`

Self explanatory.
```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
WHISPER  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat WHISPER 
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/srfi-lib/srfi/%3a60/compiled
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/racket/pkgs/srfi-lib/srfi/%3a60/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/srfi-lib/srfi/%3a60/compiled$ ls
TIP  integer-bits_rkt.dep  integer-bits_rkt.zo
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/srfi-lib/srfi/%3a60/compiled$ cat TIP
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/flask/json

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/srfi-lib/srfi/%3a60/compiled$ ls /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/flask/json
NUGGET-TRAPPED  __init__.pyi  tag.pyi
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/srfi-lib/srfi/%3a60/compiled$ cat /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/flask/json/NUGGET-TRAPPED 
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/sound/atmel
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/srfi-lib/srfi/%3a60/compiled$ cd /opt/linux/linux-5.4/sound/atmel
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/sound/atmel$ ls
Kconfig  Makefile  NOTE  ac97c.c  ac97c.h  built-in.a
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/sound/atmel$ cat NOTE
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Neo-Euler/Variants

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/sound/atmel$ cd /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Neo-Euler/Variants
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Neo-Euler/Variants$ ls -a
.  ..  .SECRET  Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Neo-Euler/Variants$ cat .SECRET 
Tubular find!
The next clue is in: /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/jinja2

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Neo-Euler/Variants$ cd /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/jinja2
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/jinja2$ ls
SNIPPET       _stringdefs.pyi  constants.pyi  environment.pyi  filters.pyi  meta.pyi       parser.pyi   tests.pyi
__init__.pyi  bccache.pyi      debug.pyi      exceptions.pyi   lexer.pyi    nodes.pyi      runtime.pyi  utils.pyi
_compat.pyi   compiler.pyi     defaults.pyi   ext.pyi          loaders.pyi  optimizer.pyi  sandbox.pyi  visitor.pyi
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/jinja2$ cat SNIPPET 
Tubular find!
The next clue is in: /opt/busybox/busybox-1.33.2/examples/var_service
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/jinja2$ cd /opt/busybox/busybox-1.33.2/examples/var_service
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/examples/var_service$ ls
ALERT                       dhcp_if         dnsmasq  getty_tty1  ifplugd_if  ntpd                sview   zcip_if
README                      dhcp_if_pinger  ftpd     gpm         inetd       std_service_logger  svpage
README_distro_proposal.txt  dhcpd_if        fw       httpd       nmeter      supplicant_if       tftpd
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/examples/var_service$ cat ALERT 
Lucky listing!
The next clue is in: /usr/share/doc/llvm

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/examples/var_service$ cd /usr/share/doc/llvm
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/llvm$ ls -a
.  ..  .CUE  NEWS.Debian.gz  README.Debian  changelog.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/llvm$ cat .CUE
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/arch/sh/cchips

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/llvm$ ls  /opt/linux/linux-5.4/arch/sh/cchips
HINT-TRAPPED  Kconfig  hd6446x
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/llvm$ cat  /opt/linux/linux-5.4/arch/sh/cchips/HINT-TRAPPED 
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{os8u_uJp4S0st_jFAEk6AX9S72i.QX5IDO0wSN3AzNzEzW}
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/llvm$ 
```

## What I learned
Reinforced `cat`, `cd`, and `ls`.

## References 
None.