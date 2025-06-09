# nmap 

```

```

# ftp login

cred: ftp : ftp

```
┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.110]
└─$ ftp 192.168.114.110
Connected to 192.168.114.110.
220 (vsFTPd 3.0.5)
Name (192.168.114.110:kali): ftp
331 Please specify the password.
Password: 
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
229 Entering Extended Passive Mode (|||38458|)


```


change to PASSIVE mode 
cd ..
ls to see a backup file 
```
ftp> ls
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
-rw-r--r--    1 1001     1002          220 Jan 06  2022 .bash_logout
-rw-r--r--    1 1001     1002         3771 Jan 06  2022 .bashrc
-rw-r--r--    1 1001     1002          807 Jan 06  2022 .profile
dr-xr-xr-x    2 1001     1002         4096 Apr 06  2023 backup
226 Directory send OK.
ftp> pwd
Remote directory: /home/ftp

```

i have 2 users, clay and lisa 
```bash 
226 Directory send OK.
ftp> pwd
Remote directory: /home
ftp> ls -alr
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
drwxrwxrwx    4 1000     1000         4096 Apr 06  2023 lisa
drwxr-x---    3 1001     1002         4096 Apr 06  2023 ftp
drwxr-x---    2 1002     1003         4096 Jul 09  2024 clay
drwxr-xr-x   19 0        0            4096 Apr 06  2023 ..
drwxr-xr-x    5 0        0            4096 Apr 06  2023 .
226 Directory send OK.
ftp> 

```

cant cd to clay but can go into lisa

```
ftp> cd clay
550 Failed to change directory.
ftp> cd lisa
250 Directory successfully changed.
ftp> 

```


lisa got some nice stuff 

```
ftp> ls -alr
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
-rw-r--r--    1 1000     1000           33 Jun 09 02:09 local.txt
drwx------    2 1000     1000         4096 Apr 06  2023 .ssh
-rw-r--r--    1 1000     1000          807 Jan 06  2022 .profile
lrwxrwxrwx    1 0        0               9 Apr 06  2023 .mysql_history -> /dev/null
drwx------    2 1000     1000         4096 Apr 06  2023 .cache
-rw-r--r--    1 1000     1000         3771 Jan 06  2022 .bashrc
-rw-r--r--    1 1000     1000          220 Jan 06  2022 .bash_logout
lrwxrwxrwx    1 0        0               9 Apr 06  2023 .bash_history -> /dev/null
drwxr-xr-x    5 0        0            4096 Apr 06  2023 ..
drwxrwxrwx    4 1000     1000         4096 Apr 06  2023 .
226 Directory send OK.
ftp> pwd
Remote directory: /home/lisa                                                                                        
ftp>                                                                                                                
                                                       
```



```

┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.110]
└─$ ftp -v 192.168.114.110
Connected to 192.168.114.110.
220 (vsFTPd 3.0.5)
Name (192.168.114.110:kali): ftp
331 Please specify the password.
Password: 
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
229 Entering Extended Passive Mode (|||40037|)
exit
^C
receive aborted. Waiting for remote to finish abort.
ftp> passive
Passive mode: off; fallback to active mode: off.
ftp> ls
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
226 Directory send OK.
ftp> ls
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
226 Directory send OK.
ftp> ls -al
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
dr-xr-xr-x    2 1001     1002         4096 Apr 06  2023 .
drwxr-x---    3 1001     1002         4096 Apr 06  2023 ..
226 Directory send OK.
ftp> ls -al ..
output to local-file: .. [anpqy?]? 
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
ftp: Can't open `..': Is a directory
226 Directory send OK.
225 No transfer to ABOR.
ftp> cd ..
250 Directory successfully changed.
ftp> ls -al
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
drwxr-x---    3 1001     1002         4096 Apr 06  2023 .
drwxr-xr-x    5 0        0            4096 Apr 06  2023 ..
-rw-r--r--    1 1001     1002          220 Jan 06  2022 .bash_logout
-rw-r--r--    1 1001     1002         3771 Jan 06  2022 .bashrc
-rw-r--r--    1 1001     1002          807 Jan 06  2022 .profile
dr-xr-xr-x    2 1001     1002         4096 Apr 06  2023 backup
226 Directory send OK.
ftp> 

```


# screenshots

![[{52191968-40D0-4ACD-920D-B56216F507C2}.png]]

![[{BA410FE9-89BF-48F9-B0F2-05FB6BAEC50E}.png]]

