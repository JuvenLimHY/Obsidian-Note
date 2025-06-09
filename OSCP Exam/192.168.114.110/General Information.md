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
# Nmap 7.95 scan initiated Mon Jun  9 09:16:57 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/_full_tcp_nmap.txt -oX /home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/xml/_full_tcp_nmap.xml 192.168.114.110
Nmap scan report for 192.168.114.110
Host is up, received user-set (0.25s latency).
Scanned at 2025-06-09 09:16:57 EDT for 647s
Not shown: 65530 filtered tcp ports (no-response)
PORT   STATE  SERVICE  REASON         VERSION
20/tcp closed ftp-data reset ttl 63
21/tcp open   ftp      syn-ack ttl 63 vsftpd 3.0.5
22/tcp open   ssh      syn-ack ttl 63 OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 a7:09:ae:7c:78:41:c7:a8:b4:41:17:20:f5:cd:15:75 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBOr5uCXt89FpAjb9GOQNcVyLaq/OHs7gLBgEF+LvgxP2PeVbxGEW9AGyohwbVwrGZ2EGJasx7N6zdTFus9MoD7c=
|   256 6c:fc:3e:2e:95:6a:54:1e:98:89:0e:c9:97:69:10:b9 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIL4oFJ6o1QVPOR4nPRBBBfiiLKBrQ1TT/RswHqeNb9sP
53/tcp closed domain   reset ttl 63
80/tcp open   http     syn-ack ttl 63 Apache httpd 2.4.52
|_http-server-header: Apache/2.4.52 (Ubuntu)
| http-methods: 
|_  Supported Methods: HEAD GET POST OPTIONS
|_http-title: Index of /
Device type: general purpose|firewall|router
Running (JUST GUESSING): Linux 4.X|5.X|6.X|3.X (97%), IPFire 2.X (91%), MikroTik RouterOS 7.X (88%)
OS CPE: cpe:/o:linux:linux_kernel:4 cpe:/o:ipfire:ipfire:2.27 cpe:/o:linux:linux_kernel:5.15 cpe:/o:linux:linux_kernel:6.1 cpe:/o:mikrotik:routeros:7 cpe:/o:linux:linux_kernel:5.6.3 cpe:/o:linux:linux_kernel:3
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 4.19 - 5.15 (97%), Linux 4.15 (92%), IPFire 2.27 (Linux 5.15 - 6.1) (91%), Linux 5.4 (90%), Linux 5.0 - 5.14 (88%), MikroTik RouterOS 7.2 - 7.5 (Linux 5.6.3) (88%), Linux 3.11 - 4.9 (88%), Linux 3.2 - 3.8 (88%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/9%OT=21%CT=20%CU=%PV=Y%DS=2%DC=T%G=N%TM=6846E150%P=x86_64-pc-linux-gnu)
SEQ(SP=104%GCD=1%ISR=10C%TI=Z%II=I%TS=A)
SEQ(SP=106%GCD=1%ISR=10D%TI=Z%II=I%TS=A)
OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 46.909 days (since Wed Apr 23 11:39:10 2025)
Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: Host: 127.0.0.1; OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 53/tcp)
HOP RTT       ADDRESS
1   248.05 ms 192.168.49.1
2   248.06 ms 192.168.114.110

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 09:27:44 2025 -- 1 IP address (1 host up) scanned in 647.70 seconds

```
### udp scan

```
# Nmap 7.95 scan initiated Mon Jun  9 09:16:57 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/_top_100_udp_nmap.txt -oX /home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/xml/_top_100_udp_nmap.xml 192.168.114.110
Nmap scan report for 192.168.114.110
Host is up, received user-set (0.30s latency).
Scanned at 2025-06-09 09:16:57 EDT for 1862s
All 100 scanned ports on 192.168.114.110 are in ignored states.
Not shown: 100 open|filtered udp ports (no-response)
Too many fingerprints match this host to give specific OS details
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/9%OT=%CT=%CU=%PV=Y%DS=2%DC=T%G=N%TM=6846E60F%P=x86_64-pc-linux-gnu)
SEQ(II=I)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Network Distance: 2 hops

TRACEROUTE (using proto 1/icmp)
HOP RTT       ADDRESS
1   299.19 ms 192.168.49.1
2   301.19 ms 192.168.114.110

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 09:47:59 2025 -- 1 IP address (1 host up) scanned in 1862.79 seconds

```

## rustscan

```

```