# Host information

```
         * Username : a.betty
         * Domain   : OSCP.EXAM
         * Password : BrightSunnyDay666

```

evil-winrm -u 'a.betty' -p 'BrightSunnyDay666' -i  172.16.114.200

# Scans
## nmap 
### quick scan

```
# Nmap 7.95 scan initiated Mon Jun  9 02:52:25 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/OSCP/Exam/AD/172.16.114.200/results/172.16.114.200/scans/_quick_tcp_nmap.txt -oX /home/kali/OSCP/Exam/AD/172.16.114.200/results/172.16.114.200/scans/xml/_quick_tcp_nmap.xml 172.16.114.200
Nmap scan report for 172.16.114.200
Host is up, received user-set (0.55s latency).
Scanned at 2025-06-09 02:52:25 EDT for 113s
Not shown: 988 filtered tcp ports (no-response)
PORT     STATE SERVICE    REASON         VERSION
53/tcp   open  tcpwrapped syn-ack ttl 64
88/tcp   open  tcpwrapped syn-ack ttl 64
135/tcp  open  tcpwrapped syn-ack ttl 64
139/tcp  open  tcpwrapped syn-ack ttl 64
389/tcp  open  tcpwrapped syn-ack ttl 64
445/tcp  open  tcpwrapped syn-ack ttl 64
464/tcp  open  tcpwrapped syn-ack ttl 64
593/tcp  open  tcpwrapped syn-ack ttl 64
636/tcp  open  tcpwrapped syn-ack ttl 64
3268/tcp open  tcpwrapped syn-ack ttl 64
3269/tcp open  tcpwrapped syn-ack ttl 64
5985/tcp open  tcpwrapped syn-ack ttl 64
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
Aggressive OS guesses: Nokia 3600i mobile phone (92%), Apple Time Capsule NAS device (92%), Cisco SF300 or SG300 switch (90%), Sony Ericsson W705 or W715 Walkman mobile phone (90%), Sony PlayStation 3 game console (88%), Cisco ATA 188 VoIP adapter (88%), Netgear SC101 Storage Central NAS device (86%), GoPro HERO3 camera (86%), Samsung CLP-310N or CLX-3175RW, or Xerox Phaser 6110 printer (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/9%OT=5985%CT=%CU=%PV=Y%G=N%TM=6846851A%P=x86_64-pc-linux-gnu)
SEQ(CI=I)
SEQ(SP=104%GCD=1%ISR=10C%TI=I%CI=I%II=RI%SS=O%TS=C)
OPS(O1=M5B4NNT11NW7%O2=M5B4NNT11NW7%O3=M5B4NNT11NW7%O4=M5B4NNT11NW7%O5=M5B4NNT11NW7%O6=M5B4NNT11)
WIN(W1=7200%W2=7200%W3=7200%W4=7200%W5=7200%W6=7200)
ECN(R=N)
ECN(R=Y%DF=N%TG=40%W=7200%O=M5B4NW7%CC=N%Q=)
T1(R=N)
T1(R=Y%DF=N%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=Y%DF=N%TG=40%W=0%S=Z%A=S%F=AR%O=%RD=0%Q=)
T3(R=N)
T3(R=Y%DF=N%TG=40%W=7200%S=O%A=S+%F=AS%O=M5B4NNT11NW7%RD=0%Q=)
T4(R=Y%DF=N%TG=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)
T6(R=Y%DF=N%TG=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)
T7(R=Y%DF=N%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
U1(R=N)
IE(R=N)
IE(R=Y%DFI=S%TG=40%CD=S)

Uptime guess: 7.334 days (since Sun Jun  1 18:53:03 2025)
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: Incremental

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 33388/tcp): CLEAN (Timeout)
|   Check 2 (port 19866/tcp): CLEAN (Timeout)
|   Check 3 (port 16821/udp): CLEAN (Timeout)
|   Check 4 (port 16642/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| nbstat: NetBIOS name: DC20, NetBIOS user: <unknown>, NetBIOS MAC: 00:50:56:8a:3a:3a (VMware)
| Names:
|   DC20<20>             Flags: <unique><active>
|   DC20<00>             Flags: <unique><active>
|   OSCP<00>             Flags: <group><active>
|   OSCP<1c>             Flags: <group><active>
|   OSCP<1b>             Flags: <unique><active>
| Statistics:
```
### full scan 

```
┌──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.200]
└─$ nmap -sV 172.16.114.200
Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-09 04:35 EDT
Nmap scan report for 172.16.114.200
Host is up (0.17s latency).
Not shown: 988 filtered tcp ports (no-response)
PORT     STATE SERVICE       VERSION
53/tcp   open  domain        Simple DNS Plus
88/tcp   open  kerberos-sec  Microsoft Windows Kerberos (server time: 2025-06-09 08:36:22Z)
135/tcp  open  msrpc         Microsoft Windows RPC
139/tcp  open  netbios-ssn   Microsoft Windows netbios-ssn
389/tcp  open  ldap          Microsoft Windows Active Directory LDAP (Domain: oscp.exam0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds?
464/tcp  open  kpasswd5?
593/tcp  open  ncacn_http    Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped
3268/tcp open  ldap          Microsoft Windows Active Directory LDAP (Domain: oscp.exam0., Site: Default-First-Site-Name)
3269/tcp open  tcpwrapped
5985/tcp open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
Service Info: Host: DC20; OS: Windows; CPE: cpe:/o:microsoft:windows

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 94.05 seconds

```
### udp scan

```

```

## rustscan

```
li㉿kali)-[~/OSCP/Exam/AD/172.16.114.200]
└─$ rustscan -a 172.16.114.200  
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
Scanning ports: The virtual equivalent of knocking on doors.

[~] The config file is expected to be at "/home/kali/.rustscan.toml"
[!] File limit is lower than default batch size. Consider upping with --ulimit. May cause harm to sensitive servers
[!] Your file limit is very small, which negatively impacts RustScan's speed. Use the Docker image, or up the Ulimit with '--ulimit 5000'. 
Open 172.16.114.200:53
Open 172.16.114.200:88
Open 172.16.114.200:139
Open 172.16.114.200:135
[~] Starting Script(s)
[~] Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-09 02:51 EDT
Initiating Ping Scan at 02:51
Scanning 172.16.114.200 [4 ports]
Completed Ping Scan at 02:51, 0.02s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 02:51
Completed Parallel DNS resolution of 1 host. at 02:51, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 02:51
Scanning 172.16.114.200 [4 ports]
Completed SYN Stealth Scan at 02:51, 1.23s elapsed (4 total ports)
Nmap scan report for 172.16.114.200
Host is up, received reset ttl 64 (0.00032s latency).
Scanned at 2025-06-09 02:51:53 EDT for 1s

PORT    STATE    SERVICE      REASON
53/tcp  filtered domain       no-response
88/tcp  filtered kerberos-sec no-response
135/tcp filtered msrpc        no-response
139/tcp filtered netbios-ssn  no-response

Read data files from: /usr/share/nmap
Nmap done: 1 IP address (1 host up) scanned in 1.35 seconds
           Raw packets sent: 12 (504B) | Rcvd: 9 (1.344KB)




```