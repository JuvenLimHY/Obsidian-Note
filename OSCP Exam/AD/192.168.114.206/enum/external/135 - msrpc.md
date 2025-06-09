# nmap 

```
# Nmap 7.95 scan initiated Sun Jun  8 22:30:59 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 135 --script=banner,msrpc-enum,rpc-grind,rpcinfo -oN /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp135/tcp_135_rpc_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp135/xml/tcp_135_rpc_nmap.xml 192.168.114.206
Nmap scan report for 192.168.114.206
Host is up, received user-set (0.25s latency).
Scanned at 2025-06-08 22:30:59 EDT for 24s

PORT    STATE SERVICE REASON          VERSION
135/tcp open  msrpc   syn-ack ttl 127 Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 22:31:23 2025 -- 1 IP address (1 host up) scanned in 24.61 seconds

```