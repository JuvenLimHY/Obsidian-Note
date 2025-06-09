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
