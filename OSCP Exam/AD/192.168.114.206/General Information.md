# Host information

```
192.168.114.206
domain: oscp.exam 
Username: r.andrews
Password: BusyOfficeWorker890
```

# Scans
## nmap 
### quick scan

```
# Nmap 7.95 scan initiated Sun Jun  8 22:23:38 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/_quick_tcp_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/xml/_quick_tcp_nmap.xml 192.168.114.206
Nmap scan report for 192.168.114.206
Host is up, received user-set (0.51s latency).
Scanned at 2025-06-08 22:23:39 EDT for 438s
Not shown: 995 filtered tcp ports (no-response)
PORT     STATE SERVICE            REASON          VERSION
135/tcp  open  msrpc              syn-ack ttl 127 Microsoft Windows RPC
139/tcp  open  netbios-ssn        syn-ack ttl 127 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds?      syn-ack ttl 127
3389/tcp open  ssl/ms-wbt-server? syn-ack ttl 127
| ssl-cert: Subject: commonName=WS26.oscp.exam
| Issuer: commonName=WS26.oscp.exam
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-11-11T12:50:39
| Not valid after:  2025-05-13T12:50:39
| MD5:   1c2c:0a0a:c19e:4426:8a74:4515:3fca:64ae
| SHA-1: cadb:9cca:0d17:b710:631b:6e7a:ebb0:d93b:5b1f:d37b
| -----BEGIN CERTIFICATE-----
| MIIC4DCCAcigAwIBAgIQJdnEr7blr7xOMCAjcMSC7zANBgkqhkiG9w0BAQsFADAZ
| MRcwFQYDVQQDEw5XUzI2Lm9zY3AuZXhhbTAeFw0yNDExMTExMjUwMzlaFw0yNTA1
| MTMxMjUwMzlaMBkxFzAVBgNVBAMTDldTMjYub3NjcC5leGFtMIIBIjANBgkqhkiG
| 9w0BAQEFAAOCAQ8AMIIBCgKCAQEAmdIbgyZ4SLJZF9YVs4dAFyQcWFOhWR5Ph738
| XQrWNhjCFCVLS0OQ4947Vq/C8XyW7Ru9PER4+/tuFL6FXbemF6iVviy2kuapC4ZX
| Rf49maAoyA80v4AxsXS76Ju19ZgJXtWhzJsBni2wPuP0WPQdqJ5WYzqZGikkdi1c
| p5wyFDw5Tk24mpgpDz3/L7WCe4qywUGNvKV7GhH/twcex+LhDiG1RMiZBxncSqAA
| jc9ZtDoO/bBmuF/c2aKNJWE/bI01gQHezOHmSYuCrsbe1IDKSeI5XHBnFwUM1ETT
| JOl4F0Z8z4FWwpNgyP/vdi/CwNEXEx3ntJ7YtC9f9YJD/JqHIQIDAQABoyQwIjAT
| BgNVHSUEDDAKBggrBgEFBQcDATALBgNVHQ8EBAMCBDAwDQYJKoZIhvcNAQELBQAD
| ggEBAGCDGtCm9fI3BqvlzdlYsqUUz0ET8ImA9xKtJpkgL+ACswzewyGDwHa9b4RD
| iU9N7hPnhIwFq9LsMENvGEzQXPfV8kVk6oASwW8vO5zK6qYTin0exu9pyNqma1uY
| a933O+OfhLsv2+ksUfgZ69hv5NExxVtRgY6toDY/OkvWEiU2u0E4rwjdHknuNj3b
| 46cqLVPChgoAN6pBdObWS7kdbXeViklsPd5yaC2JJH48DHA2NXpKuH5aJgmwROs/
| yFxPxbx2d9xYcjJLpbuNyv5akeyjfMijr1pksHASN3k7tNTnswzlJjrd82vZVY5j
| 6aUtAEe1VGnMsXSQzkyxqpO/Dgw=
|_-----END CERTIFICATE-----
|_ssl-date: TLS randomness does not represent time
| rdp-ntlm-info: 
|   Target_Name: OSCP
|   NetBIOS_Domain_Name: OSCP
|   NetBIOS_Computer_Name: WS26
|   DNS_Domain_Name: oscp.exam
|   DNS_Computer_Name: WS26.oscp.exam
|   DNS_Tree_Name: oscp.exam
|   Product_Version: 10.0.22621
|_  System_Time: 2024-11-12T13:09:53+00:00
5985/tcp open  http               syn-ack ttl 127 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows 11|2008|7|2016 (89%)
OS CPE: cpe:/o:microsoft:windows_11 cpe:/o:microsoft:windows_server_2008:r2 cpe:/o:microsoft:windows_7 cpe:/o:microsoft:windows_server_2016
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
Aggressive OS guesses: Microsoft Windows 11 21H2 (89%), Microsoft Windows 7 or Windows Server 2008 R2 (85%), Microsoft Windows Server 2016 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/8%OT=135%CT=%CU=%PV=Y%DS=2%DC=T%G=N%TM=68464761%P=x86_64-pc-linux-gnu)
SEQ(SP=108%GCD=1%ISR=10B%TI=I%II=I%SS=S%TS=A)
SEQ(SP=FD%GCD=1%ISR=10F%TI=I%II=I%SS=S%TS=A)
OPS(O1=M551NW8ST11%O2=M551NW8ST11%O3=M551NW8NNT11%O4=M551NW8ST11%O5=M551NW8ST11%O6=M551ST11)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FFDC)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=N%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=80%CD=Z)

Uptime guess: 0.025 days (since Sun Jun  8 21:54:17 2025)
Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=253 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: -208d13h20m23s, deviation: 0s, median: -208d13h20m23s
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2024-11-12T13:09:55
|_  start_date: N/A
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 16744/tcp): CLEAN (Timeout)
|   Check 2 (port 49411/tcp): CLEAN (Timeout)
|   Check 3 (port 31065/udp): CLEAN (Timeout)
|   Check 4 (port 51316/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked

TRACEROUTE (using port 3389/tcp)
HOP RTT       ADDRESS
1   ...
2   679.51 ms 192.168.114.206

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 22:30:57 2025 -- 1 IP address (1 host up) scanned in 438.96 seconds

```
### full scan 

```
# Nmap 7.95 scan initiated Sun Jun  8 22:23:38 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/_full_tcp_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/xml/_full_tcp_nmap.xml 192.168.114.206
Nmap scan report for 192.168.114.206
Host is up, received user-set (0.24s latency).
Scanned at 2025-06-08 22:23:39 EDT for 671s
Not shown: 65530 filtered tcp ports (no-response)
PORT     STATE SERVICE            REASON          VERSION
135/tcp  open  msrpc              syn-ack ttl 127 Microsoft Windows RPC
139/tcp  open  netbios-ssn        syn-ack ttl 127 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds?      syn-ack ttl 127
3389/tcp open  ssl/ms-wbt-server? syn-ack ttl 127
| ssl-cert: Subject: commonName=WS26.oscp.exam
| Issuer: commonName=WS26.oscp.exam
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2024-11-11T12:50:39
| Not valid after:  2025-05-13T12:50:39
| MD5:   1c2c:0a0a:c19e:4426:8a74:4515:3fca:64ae
| SHA-1: cadb:9cca:0d17:b710:631b:6e7a:ebb0:d93b:5b1f:d37b
| -----BEGIN CERTIFICATE-----
| MIIC4DCCAcigAwIBAgIQJdnEr7blr7xOMCAjcMSC7zANBgkqhkiG9w0BAQsFADAZ
| MRcwFQYDVQQDEw5XUzI2Lm9zY3AuZXhhbTAeFw0yNDExMTExMjUwMzlaFw0yNTA1
| MTMxMjUwMzlaMBkxFzAVBgNVBAMTDldTMjYub3NjcC5leGFtMIIBIjANBgkqhkiG
| 9w0BAQEFAAOCAQ8AMIIBCgKCAQEAmdIbgyZ4SLJZF9YVs4dAFyQcWFOhWR5Ph738
| XQrWNhjCFCVLS0OQ4947Vq/C8XyW7Ru9PER4+/tuFL6FXbemF6iVviy2kuapC4ZX
| Rf49maAoyA80v4AxsXS76Ju19ZgJXtWhzJsBni2wPuP0WPQdqJ5WYzqZGikkdi1c
| p5wyFDw5Tk24mpgpDz3/L7WCe4qywUGNvKV7GhH/twcex+LhDiG1RMiZBxncSqAA
| jc9ZtDoO/bBmuF/c2aKNJWE/bI01gQHezOHmSYuCrsbe1IDKSeI5XHBnFwUM1ETT
| JOl4F0Z8z4FWwpNgyP/vdi/CwNEXEx3ntJ7YtC9f9YJD/JqHIQIDAQABoyQwIjAT
| BgNVHSUEDDAKBggrBgEFBQcDATALBgNVHQ8EBAMCBDAwDQYJKoZIhvcNAQELBQAD
| ggEBAGCDGtCm9fI3BqvlzdlYsqUUz0ET8ImA9xKtJpkgL+ACswzewyGDwHa9b4RD
| iU9N7hPnhIwFq9LsMENvGEzQXPfV8kVk6oASwW8vO5zK6qYTin0exu9pyNqma1uY
| a933O+OfhLsv2+ksUfgZ69hv5NExxVtRgY6toDY/OkvWEiU2u0E4rwjdHknuNj3b
| 46cqLVPChgoAN6pBdObWS7kdbXeViklsPd5yaC2JJH48DHA2NXpKuH5aJgmwROs/
| yFxPxbx2d9xYcjJLpbuNyv5akeyjfMijr1pksHASN3k7tNTnswzlJjrd82vZVY5j
| 6aUtAEe1VGnMsXSQzkyxqpO/Dgw=
|_-----END CERTIFICATE-----
|_ssl-date: TLS randomness does not represent time
| rdp-ntlm-info: 
|   Target_Name: OSCP
|   NetBIOS_Domain_Name: OSCP
|   NetBIOS_Computer_Name: WS26
|   DNS_Domain_Name: oscp.exam
|   DNS_Computer_Name: WS26.oscp.exam
|   DNS_Tree_Name: oscp.exam
|   Product_Version: 10.0.22621
|_  System_Time: 2024-11-12T13:13:46+00:00
5985/tcp open  http               syn-ack ttl 127 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows 11|2008|7|2016 (89%)
OS CPE: cpe:/o:microsoft:windows_11 cpe:/o:microsoft:windows_server_2008:r2 cpe:/o:microsoft:windows_7 cpe:/o:microsoft:windows_server_2016
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
Aggressive OS guesses: Microsoft Windows 11 21H2 (89%), Microsoft Windows 7 or Windows Server 2008 R2 (85%), Microsoft Windows Server 2016 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/8%OT=135%CT=%CU=%PV=Y%DS=2%DC=T%G=N%TM=6846484A%P=x86_64-pc-linux-gnu)
SEQ(SP=102%GCD=1%ISR=10B%TI=I%II=I%SS=S%TS=A)
SEQ(SP=106%GCD=1%ISR=10B%TI=I%II=I%SS=S%TS=A)
OPS(O1=M551NW8ST11%O2=M551NW8ST11%O3=M551NW8NNT11%O4=M551NW8ST11%O5=M551NW8ST11%O6=M551ST11)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FFDC)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=N%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=80%CD=Z)

Uptime guess: 0.028 days (since Sun Jun  8 21:54:17 2025)
Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=258 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 16744/tcp): CLEAN (Timeout)
|   Check 2 (port 49411/tcp): CLEAN (Timeout)
|   Check 3 (port 31065/udp): CLEAN (Timeout)
|   Check 4 (port 51316/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
|_clock-skew: mean: -208d13h20m22s, deviation: 0s, median: -208d13h20m22s
| smb2-time: 
|   date: 2024-11-12T13:13:50
|_  start_date: N/A
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required

TRACEROUTE (using port 139/tcp)
HOP RTT       ADDRESS
1   242.09 ms 192.168.49.1
2   242.11 ms 192.168.114.206

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 22:34:50 2025 -- 1 IP address (1 host up) scanned in 671.97 seconds

```
### udp scan

```
# Nmap 7.95 scan initiated Sun Jun  8 22:23:38 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/_top_100_udp_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/xml/_top_100_udp_nmap.xml 192.168.114.206
Nmap scan report for 192.168.114.206
Host is up, received user-set (0.30s latency).
Scanned at 2025-06-08 22:23:39 EDT for 1824s
All 100 scanned ports on 192.168.114.206 are in ignored states.
Not shown: 100 open|filtered udp ports (no-response)
Too many fingerprints match this host to give specific OS details
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/8%OT=%CT=%CU=%PV=Y%DS=2%DC=T%G=N%TM=68464CCB%P=x86_64-pc-linux-gnu)
SEQ(II=I)
U1(R=N)
IE(R=Y%DFI=N%TG=80%CD=Z)

Network Distance: 2 hops

TRACEROUTE (using proto 1/icmp)
HOP RTT       ADDRESS
1   319.96 ms 192.168.49.1
2   320.34 ms 192.168.114.206

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 22:54:03 2025 -- 1 IP address (1 host up) scanned in 1824.27 seconds

```

## rustscan

```
┌──(kali㉿kali)-[~/OSCP/Exam/AD/192.168.114.206]
└─$ rustscan -a 192.168.114.206                                
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
Open ports, closed hearts.

[~] The config file is expected to be at "/home/kali/.rustscan.toml"
[!] File limit is lower than default batch size. Consider upping with --ulimit. May cause harm to sensitive servers
[!] Your file limit is very small, which negatively impacts RustScan's speed. Use the Docker image, or up the Ulimit with '--ulimit 5000'. 
Open 192.168.114.206:135
Open 192.168.114.206:139
Open 192.168.114.206:445
Open 192.168.114.206:3389
Open 192.168.114.206:5985
[~] Starting Script(s)
[~] Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-08 22:28 EDT
Initiating Ping Scan at 22:28
Scanning 192.168.114.206 [4 ports]
Completed Ping Scan at 22:28, 0.27s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 22:28
Completed Parallel DNS resolution of 1 host. at 22:28, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 22:28
Scanning 192.168.114.206 [5 ports]
Discovered open port 139/tcp on 192.168.114.206
Discovered open port 3389/tcp on 192.168.114.206
Discovered open port 135/tcp on 192.168.114.206
Discovered open port 445/tcp on 192.168.114.206
Discovered open port 5985/tcp on 192.168.114.206
Completed SYN Stealth Scan at 22:28, 0.26s elapsed (5 total ports)
Nmap scan report for 192.168.114.206
Host is up, received echo-reply ttl 127 (0.24s latency).
Scanned at 2025-06-08 22:28:30 EDT for 0s

PORT     STATE SERVICE       REASON
135/tcp  open  msrpc         syn-ack ttl 127
139/tcp  open  netbios-ssn   syn-ack ttl 127
445/tcp  open  microsoft-ds  syn-ack ttl 127
3389/tcp open  ms-wbt-server syn-ack ttl 127
5985/tcp open  wsman         syn-ack ttl 127

Read data files from: /usr/share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.65 seconds
           Raw packets sent: 9 (372B) | Rcvd: 6 (248B)

```

# Things to try 

```
[*] msrpc on tcp/135

	[-] RPC Client:

		rpcclient -p 135 -U "" 192.168.114.206

[*] netbios-ssn on tcp/139

	[-] Bruteforce SMB

		crackmapexec smb 192.168.114.206 --port=139 -u "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -p "/usr/share/seclists/Passwords/darkweb2017-top100.txt"

	[-] Nmap scans for SMB vulnerabilities that could potentially cause a DoS if scanned (according to Nmap). Be careful:

		nmap -vv --reason -Pn -T4 -sV -p 139 --script="smb-vuln-* and dos" --script-args="unsafe=1" -oN "/home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp139/tcp_139_smb_vulnerabilities.txt" -oX "/home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp139/xml/tcp_139_smb_vulnerabilities.xml" 192.168.114.206

[*] microsoft-ds on tcp/445

	[-] Bruteforce SMB

		crackmapexec smb 192.168.114.206 --port=445 -u "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -p "/usr/share/seclists/Passwords/darkweb2017-top100.txt"

	[-] Lookup SIDs

		impacket-lookupsid '[username]:[password]@192.168.114.206'

	[-] Nmap scans for SMB vulnerabilities that could potentially cause a DoS if scanned (according to Nmap). Be careful:

		nmap -vv --reason -Pn -T4 -sV -p 445 --script="smb-vuln-* and dos" --script-args="unsafe=1" -oN "/home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp445/tcp_445_smb_vulnerabilities.txt" -oX "/home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp445/xml/tcp_445_smb_vulnerabilities.xml" 192.168.114.206

[*] ms-wbt-server on tcp/3389

	[-] Bruteforce logins:

		hydra -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e nsr -s 3389 -o "/home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp3389/tcp_3389_rdp_hydra.txt" rdp://192.168.114.206

		medusa -U "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e ns -n 3389 -O "/home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp3389/tcp_3389_rdp_medusa.txt" -M rdp -h 192.168.114.206

[*] wsman on tcp/5985

	[-] Bruteforce logins:

		crackmapexec winrm 192.168.114.206 -d '<domain>' -u '/usr/share/seclists/Usernames/top-usernames-shortlist.txt' -p '/usr/share/seclists/Passwords/darkweb2017-top100.txt'

	[-] Check login (requires credentials):

		crackmapexec winrm 192.168.114.206 -d '<domain>' -u '<username>' -p '<password>'

	[-] Evil WinRM (gem install evil-winrm):

		evil-winrm -u '<user>' -p '<password>' -i 192.168.114.206

		evil-winrm -u '<user>' -H '<hash>' -i 192.168.114.206


```