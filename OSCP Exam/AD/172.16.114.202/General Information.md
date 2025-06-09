# Host information

```

```

# Scans
## nmap 
### quick scan

```
# Nmap 7.95 scan initiated Mon Jun  9 02:52:45 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/OSCP/Exam/AD/172.16.114.202/results/172.16.114.202/scans/_quick_tcp_nmap.txt -oX /home/kali/OSCP/Exam/AD/172.16.114.202/results/172.16.114.202/scans/xml/_quick_tcp_nmap.xml 172.16.114.202
Nmap scan report for 172.16.114.202
Host is up, received user-set (0.38s latency).
Scanned at 2025-06-09 02:52:45 EDT for 110s
Not shown: 996 filtered tcp ports (no-response)
PORT     STATE SERVICE    REASON         VERSION
135/tcp  open  tcpwrapped syn-ack ttl 64
139/tcp  open  tcpwrapped syn-ack ttl 64
445/tcp  open  tcpwrapped syn-ack ttl 64
5985/tcp open  tcpwrapped syn-ack ttl 64
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/9%OT=5985%CT=%CU=%PV=Y%G=N%TM=6846852B%P=x86_64-pc-linux-gnu)
SEQ(SP=101%GCD=1%ISR=10C%TI=RD%CI=I%II=RI%TS=9)
SEQ(SP=105%GCD=1%ISR=10B%TI=RD%CI=I%TS=A)
OPS(O1=M5B4NNT11NW7%O2=M5B4NNT11NW7%O3=M5B4NNT11NW7%O4=M5B4NNT11NW7%O5=M5B4NNT11NW7%O6=M5B4NNT11)
WIN(W1=7200%W2=7200%W3=7200%W4=7200%W5=7200%W6=7200)
ECN(R=Y%DF=N%TG=40%W=7200%O=M5B4NW7%CC=N%Q=)
T1(R=Y%DF=N%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=Y%DF=N%TG=40%W=0%S=Z%A=S%F=AR%O=%RD=0%Q=)
T3(R=Y%DF=N%TG=40%W=7200%S=O%A=S+%F=AS%O=M5B4NNT11NW7%RD=0%Q=)
T4(R=Y%DF=N%TG=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)
T6(R=Y%DF=N%TG=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)
T7(R=Y%DF=N%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
U1(R=N)
IE(R=Y%DFI=S%TG=40%CD=S)

Uptime guess: 6.912 days (since Mon Jun  2 05:01:20 2025)
TCP Sequence Prediction: Difficulty=257 (Good luck!)
IP ID Sequence Generation: Randomized

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 28687/tcp): CLEAN (Timeout)
|   Check 2 (port 5728/tcp): CLEAN (Timeout)
|   Check 3 (port 57215/udp): CLEAN (Timeout)
|   Check 4 (port 33981/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-time: 
|   date: 2025-06-09T06:54:03
|_  start_date: N/A
|_clock-skew: -3s

TRACEROUTE
HOP RTT       ADDRESS
1   380.46 ms 172.16.114.202

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 02:54:35 2025 -- 1 IP address (1 host up) scanned in 110.41 seconds

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