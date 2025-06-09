# Host information

```

```

# Scans
## nmap 
### quick scan

```

```
### full scan 

```

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