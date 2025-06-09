# Host information

```

```

# Scans
## nmap 
### quick scan

```
┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.110]
└─$ nmap -sV 192.168.114.110                                                                               
Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-09 09:04 EDT
Nmap scan report for 192.168.114.110
Host is up (0.25s latency).
Not shown: 995 filtered tcp ports (no-response)
PORT   STATE  SERVICE  VERSION
20/tcp closed ftp-data
21/tcp open   ftp      vsftpd 3.0.5
22/tcp open   ssh      OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
53/tcp closed domain
80/tcp open   http     Apache httpd 2.4.52
Service Info: Host: 127.0.0.1; OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 23.96 seconds
                                                                
```
### full scan 

```

```
### udp scan

```

```

## rustscan

```

```