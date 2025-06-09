# Host information

```

```

# Scans
## nmap 
### quick scan

```
# Nmap 7.95 scan initiated Mon Jun  9 10:30:09 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/_quick_tcp_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/xml/_quick_tcp_nmap.xml 192.168.114.111
Warning: Hit PCRE_ERROR_MATCHLIMIT when probing for service http with the regex '^HTTP/1\.1 \d\d\d (?:[^\r\n]*\r\n(?!\r\n))*?.*\r\nServer: Virata-EmWeb/R([\d_]+)\r\nContent-Type: text/html; ?charset=UTF-8\r\nExpires: .*<title>HP (Color |)LaserJet ([\w._ -]+)&nbsp;&nbsp;&nbsp;'
Nmap scan report for 192.168.114.111
Host is up, received user-set (0.25s latency).
Scanned at 2025-06-09 10:30:10 EDT for 62s
Not shown: 996 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
21/tcp   open  ftp           syn-ack ttl 127 Microsoft ftpd
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_Can't get directory listing: TIMEOUT
| ftp-syst: 
|_  SYST: Windows_NT
80/tcp   open  http          syn-ack ttl 127 Microsoft IIS httpd 10.0
|_http-title: Home
|_http-server-header: Microsoft-IIS/10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-generator: Nicepage 4.16.0, nicepage.com
3389/tcp open  ms-wbt-server syn-ack ttl 127 Microsoft Terminal Services
| ssl-cert: Subject: commonName=OSCP
| Issuer: commonName=OSCP
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2025-06-08T02:28:18
| Not valid after:  2025-12-08T02:28:18
| MD5:   d6a4:2b2b:b2f2:7132:fccd:331d:6957:6831
| SHA-1: f26b:a83e:1e5d:2f4f:0257:77d9:db23:f924:fbb0:0562
| -----BEGIN CERTIFICATE-----
| MIICzDCCAbSgAwIBAgIQH/3u4/PpcKdHCs3xI1tmOjANBgkqhkiG9w0BAQsFADAP
| MQ0wCwYDVQQDEwRPU0NQMB4XDTI1MDYwODAyMjgxOFoXDTI1MTIwODAyMjgxOFow
| DzENMAsGA1UEAxMET1NDUDCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEB
| ANWaJpKcSZNWIGt+WSDx1FfkSBPd8g4EHGADXZcvU9Gar3Nr5GLMcl0UFSc78Dwd
| mf/yhdk7ckIkdvQVj1fST3ZZmgxgfVp3XPjvpx8rBhK0hOlXaUngo/12Vwwyvuyy
| 4Knsj13KxeSiN9t4ynypg+z0jMqksMXOq8PaMRqX8eivZrlh8DbrmsX8zRtC+ujA
| CNxpi+xYIG0URALceRdE6Fi+C6hMZlVIYqEY8oIp5tQkOFFqlr0MvbEhxaA8yvR7
| tM3miDTiHUfjYNdklaOQfBS30RhE5/xSUmUnDmfwph/VzGc44CrVJB9LlhSW0VvX
| 1TPomaeYl6+7lGj/GqAnaJ0CAwEAAaMkMCIwEwYDVR0lBAwwCgYIKwYBBQUHAwEw
| CwYDVR0PBAQDAgQwMA0GCSqGSIb3DQEBCwUAA4IBAQAFfB5aACB6yV+QmvoXXFdF
| QTcWTviCE5fnaWei1RwXOlmJ2L/EmQaq312EYVWyqlqkonUQwauszAN/Ni+7T/vp
| 87cwRB3EPF7vZtwF+WDepQ4Yu7mprIFfjdhi5hsxS0KRQH+BYvWtNgHLeObDrAIi
| ab1+y0LKpi115/6tCKf/DFfXm5gRmryyEVUlsMNI+DkSq6IgqgqLBdiGpyTMXmbX
| yWinHVRd33PVQNbTVn9802AsHcLYf71jg6yA5V5m1D+0cNGwxLJzi5zWAROxN86E
| iq7/olr+cZDR6rI6xoZ1p6rnl+HsISDZSsgpSX2UvFATQ6408YADiPHjVWfAf0Jj
|_-----END CERTIFICATE-----
|_ssl-date: 2025-06-09T14:31:11+00:00; +1s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: OSCP
|   NetBIOS_Domain_Name: OSCP
|   NetBIOS_Computer_Name: OSCP
|   DNS_Domain_Name: OSCP
|   DNS_Computer_Name: OSCP
|   Product_Version: 10.0.19041
|_  System_Time: 2025-06-09T14:30:40+00:00
8080/tcp open  http          syn-ack ttl 127 Microsoft IIS httpd 10.0
|_http-open-proxy: Proxy might be redirecting requests
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-title: IIS Windows
|_http-server-header: Microsoft-IIS/10.0
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows 10|2019 (92%)
OS CPE: cpe:/o:microsoft:windows_10 cpe:/o:microsoft:windows_server_2019
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
Aggressive OS guesses: Microsoft Windows 10 1903 - 21H1 (92%), Microsoft Windows 10 1909 - 2004 (85%), Windows Server 2019 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/9%OT=21%CT=%CU=%PV=Y%DS=2%DC=T%G=N%TM=6846F030%P=x86_64-pc-linux-gnu)
SEQ(SP=102%GCD=1%ISR=10D%TI=I%TS=U)
SEQ(SP=106%GCD=1%ISR=10E%TI=I%TS=U)
OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=N%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=N)

Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 0s, deviation: 0s, median: 0s

TRACEROUTE (using port 80/tcp)
HOP RTT       ADDRESS
1   257.03 ms 192.168.49.1
2   257.06 ms 192.168.114.111

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 10:31:12 2025 -- 1 IP address (1 host up) scanned in 62.49 seconds

```
### full scan 

```
# Nmap 7.95 scan initiated Mon Jun  9 10:30:09 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/_full_tcp_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/xml/_full_tcp_nmap.xml 192.168.114.111
Warning: Hit PCRE_ERROR_MATCHLIMIT when probing for service http with the regex '^HTTP/1\.1 \d\d\d (?:[^\r\n]*\r\n(?!\r\n))*?.*\r\nServer: Virata-EmWeb/R([\d_]+)\r\nContent-Type: text/html; ?charset=UTF-8\r\nExpires: .*<title>HP (Color |)LaserJet ([\w._ -]+)&nbsp;&nbsp;&nbsp;'
Nmap scan report for 192.168.114.111
Host is up, received user-set (0.24s latency).
Scanned at 2025-06-09 10:30:10 EDT for 406s
Not shown: 65531 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
21/tcp   open  ftp           syn-ack ttl 127 Microsoft ftpd
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_Can't get directory listing: TIMEOUT
| ftp-syst: 
|_  SYST: Windows_NT
80/tcp   open  http          syn-ack ttl 127 Microsoft IIS httpd 10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
|_http-generator: Nicepage 4.16.0, nicepage.com
|_http-title: Home
3389/tcp open  ms-wbt-server syn-ack ttl 127 Microsoft Terminal Services
|_ssl-date: 2025-06-09T14:36:55+00:00; +1s from scanner time.
| ssl-cert: Subject: commonName=OSCP
| Issuer: commonName=OSCP
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2025-06-08T02:28:18
| Not valid after:  2025-12-08T02:28:18
| MD5:   d6a4:2b2b:b2f2:7132:fccd:331d:6957:6831
| SHA-1: f26b:a83e:1e5d:2f4f:0257:77d9:db23:f924:fbb0:0562
| -----BEGIN CERTIFICATE-----
| MIICzDCCAbSgAwIBAgIQH/3u4/PpcKdHCs3xI1tmOjANBgkqhkiG9w0BAQsFADAP
| MQ0wCwYDVQQDEwRPU0NQMB4XDTI1MDYwODAyMjgxOFoXDTI1MTIwODAyMjgxOFow
| DzENMAsGA1UEAxMET1NDUDCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEB
| ANWaJpKcSZNWIGt+WSDx1FfkSBPd8g4EHGADXZcvU9Gar3Nr5GLMcl0UFSc78Dwd
| mf/yhdk7ckIkdvQVj1fST3ZZmgxgfVp3XPjvpx8rBhK0hOlXaUngo/12Vwwyvuyy
| 4Knsj13KxeSiN9t4ynypg+z0jMqksMXOq8PaMRqX8eivZrlh8DbrmsX8zRtC+ujA
| CNxpi+xYIG0URALceRdE6Fi+C6hMZlVIYqEY8oIp5tQkOFFqlr0MvbEhxaA8yvR7
| tM3miDTiHUfjYNdklaOQfBS30RhE5/xSUmUnDmfwph/VzGc44CrVJB9LlhSW0VvX
| 1TPomaeYl6+7lGj/GqAnaJ0CAwEAAaMkMCIwEwYDVR0lBAwwCgYIKwYBBQUHAwEw
| CwYDVR0PBAQDAgQwMA0GCSqGSIb3DQEBCwUAA4IBAQAFfB5aACB6yV+QmvoXXFdF
| QTcWTviCE5fnaWei1RwXOlmJ2L/EmQaq312EYVWyqlqkonUQwauszAN/Ni+7T/vp
| 87cwRB3EPF7vZtwF+WDepQ4Yu7mprIFfjdhi5hsxS0KRQH+BYvWtNgHLeObDrAIi
| ab1+y0LKpi115/6tCKf/DFfXm5gRmryyEVUlsMNI+DkSq6IgqgqLBdiGpyTMXmbX
| yWinHVRd33PVQNbTVn9802AsHcLYf71jg6yA5V5m1D+0cNGwxLJzi5zWAROxN86E
| iq7/olr+cZDR6rI6xoZ1p6rnl+HsISDZSsgpSX2UvFATQ6408YADiPHjVWfAf0Jj
|_-----END CERTIFICATE-----
| rdp-ntlm-info: 
|   Target_Name: OSCP
|   NetBIOS_Domain_Name: OSCP
|   NetBIOS_Computer_Name: OSCP
|   DNS_Domain_Name: OSCP
|   DNS_Computer_Name: OSCP
|   Product_Version: 10.0.19041
|_  System_Time: 2025-06-09T14:36:24+00:00
8080/tcp open  http          syn-ack ttl 127 Microsoft IIS httpd 10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-title: IIS Windows
|_http-open-proxy: Proxy might be redirecting requests
|_http-server-header: Microsoft-IIS/10.0
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows 10 (92%)
OS CPE: cpe:/o:microsoft:windows_10
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
Aggressive OS guesses: Microsoft Windows 10 1903 - 21H1 (92%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/9%OT=21%CT=%CU=%PV=Y%DS=2%DC=T%G=N%TM=6846F188%P=x86_64-pc-linux-gnu)
SEQ(SP=102%GCD=1%ISR=10D%TS=U)
SEQ(SP=106%GCD=1%ISR=10E%TS=U)
OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=N%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=N)

Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 0s, deviation: 0s, median: 0s

TRACEROUTE (using port 80/tcp)
HOP RTT       ADDRESS
1   244.25 ms 192.168.49.1
2   244.27 ms 192.168.114.111

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 10:36:56 2025 -- 1 IP address (1 host up) scanned in 406.91 seconds

```
### udp scan

```
# Nmap 7.95 scan initiated Mon Jun  9 10:30:09 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/_top_100_udp_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/xml/_top_100_udp_nmap.xml 192.168.114.111
Nmap scan report for 192.168.114.111
Host is up, received user-set.
Scanned at 2025-06-09 10:30:10 EDT for 1833s
All 100 scanned ports on 192.168.114.111 are in ignored states.
Not shown: 100 open|filtered udp ports (no-response)
Too many fingerprints match this host to give specific OS details
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/9%OT=%CT=%CU=%PV=Y%G=N%TM=6846F71B%P=x86_64-pc-linux-gnu)
SEQ()
U1(R=N)
IE(R=N)


TRACEROUTE (using proto 1/icmp)
HOP RTT       ADDRESS
1   247.45 ms 192.168.49.1
2   ... 30

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 11:00:43 2025 -- 1 IP address (1 host up) scanned in 1834.08 seconds

```

## rustscan

```
──(kali㉿kali)-[~/OSCP/Exam/AD/192.168.114.111]
└─$ rustscan -a 192.168.114.111                                                                            
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
RustScan: Where '404 Not Found' meets '200 OK'.

[~] The config file is expected to be at "/home/kali/.rustscan.toml"
[!] File limit is lower than default batch size. Consider upping with --ulimit. May cause harm to sensitive servers
[!] Your file limit is very small, which negatively impacts RustScan's speed. Use the Docker image, or up the Ulimit
Open 192.168.114.111:21
Open 192.168.114.111:80
Open 192.168.114.111:3389
Open 192.168.114.111:8080
[~] Starting Script(s)
[~] Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-09 10:32 EDT
Initiating Ping Scan at 10:32
Scanning 192.168.114.111 [4 ports]
Completed Ping Scan at 10:32, 3.04s elapsed (1 total hosts)
Nmap scan report for 192.168.114.111 [host down, received no-response]
Read data files from: /usr/share/nmap
Note: Host seems down. If it is really up, but blocking our ping probes, try -Pn
Nmap done: 1 IP address (0 hosts up) scanned in 3.10 seconds
           Raw packets sent: 8 (304B) | Rcvd: 1583 (338.267KB)


```