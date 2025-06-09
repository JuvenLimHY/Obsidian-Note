# nmap 

```
# Nmap 7.95 scan initiated Mon Jun  9 10:31:12 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 21 "--script=banner,(ftp* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/tcp21/tcp_21_ftp_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/tcp21/xml/tcp_21_ftp_nmap.xml 192.168.114.111
Nmap scan report for 192.168.114.111
Host is up, received user-set (0.25s latency).
Scanned at 2025-06-09 10:31:12 EDT for 35s

PORT   STATE SERVICE REASON          VERSION
21/tcp open  ftp     syn-ack ttl 127 Microsoft ftpd
|_banner: 220 Microsoft FTP Service
| ftp-syst: 
|_  SYST: Windows_NT
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_Can't get directory listing: TIMEOUT
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 10:31:47 2025 -- 1 IP address (1 host up) scanned in 34.90 seconds

```


login via 
anonymous 

![[{721BF4BC-5C3A-4FD2-8109-6F4C733EE070} 1.png]]

```
┌──(kali㉿kali)-[~/OSCP/Exam/AD/192.168.114.111]
└─$ ftp 192.168.114.111
Connected to 192.168.114.111.
220 Microsoft FTP Service
Name (192.168.114.111:kali): anonymous
331 Anonymous access allowed, send identity (e-mail name) as password.
Password: 
230 User logged in.
Remote system type is Windows_NT.
ftp> ls
229 Entering Extended Passive Mode (|||50944|)
exit
^C
receive aborted. Waiting for remote to finish abort.
ftp> passive
Passive mode: off; fallback to active mode: off.
ftp> ls
200 EPRT command successful.
150 Opening ASCII mode data connection.
425 Cannot open data connection.
ftp> ls -alr
200 EPRT command successful.
125 Data connection already open; Transfer starting.
12-07-19  02:12AM                  278 desktop.ini
08-29-22  04:06PM       <DIR>          My Music
08-29-22  04:06PM       <DIR>          My Pictures
08-29-22  04:06PM       <DIR>          My Videos
08-31-22  03:14PM       <DIR>          SanDisk
226 Transfer complete.
ftp> cd SanDisk
250 CWD command successful.
ftp> ls alr
200 EPRT command successful.
550 The system cannot find the file specified. 
ftp> ls -alr
200 EPRT command successful.
125 Data connection already open; Transfer starting.
08-31-22  03:01PM                    4 ._DS_Store
08-31-22  03:12PM               705638 BackUp.zip
08-31-22  03:09PM                90587 Inventory.xls
08-31-22  03:09PM                62822 LeaveApplicationForm.pdf
08-31-22  02:56PM                22084 MyKeychain.keychain-db
08-31-22  03:10PM                75587 Salaries.xlsx

```

