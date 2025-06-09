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
┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.112]
└─$ rustscan -a 192.168.114.112 
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
RustScan: Because guessing isn't hacking.

[~] The config file is expected to be at "/home/kali/.rustscan.toml"
[!] File limit is lower than default batch size. Consider upping with --ulimit. May cause harm to sensitive servers
[!] Your file limit is very small, which negatively impacts RustScan's speed. Use the Docker image, or up the Ulimit
Open 192.168.114.112:21
Open 192.168.114.112:22
Open 192.168.114.112:80
Open 192.168.114.112:139
Open 192.168.114.112:445
[~] Starting Script(s)
[~] Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-09 12:06 EDT
Initiating Ping Scan at 12:06
Scanning 192.168.114.112 [4 ports]
Completed Ping Scan at 12:06, 0.29s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 12:06
Completed Parallel DNS resolution of 1 host. at 12:06, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 12:06
Scanning 192.168.114.112 [5 ports]
Discovered open port 139/tcp on 192.168.114.112
Discovered open port 445/tcp on 192.168.114.112
Discovered open port 22/tcp on 192.168.114.112
Discovered open port 80/tcp on 192.168.114.112
Discovered open port 21/tcp on 192.168.114.112
Completed SYN Stealth Scan at 12:06, 0.26s elapsed (5 total ports)
Nmap scan report for 192.168.114.112
Host is up, received echo-reply ttl 63 (0.25s latency).
Scanned at 2025-06-09 12:06:57 EDT for 0s

PORT    STATE SERVICE      REASON
21/tcp  open  ftp          syn-ack ttl 63
22/tcp  open  ssh          syn-ack ttl 63
80/tcp  open  http         syn-ack ttl 63
139/tcp open  netbios-ssn  syn-ack ttl 63
445/tcp open  microsoft-ds syn-ack ttl 63

Read data files from: /usr/share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.66 seconds
           Raw packets sent: 9 (372B) | Rcvd: 6 (248B)


```