# nmap 

```
# Nmap 7.95 scan initiated Sun Jun  8 22:30:59 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp139/tcp_139_smb_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp139/xml/tcp_139_smb_nmap.xml 192.168.114.206
Nmap scan report for 192.168.114.206
Host is up, received user-set.
Scanned at 2025-06-08 22:30:59 EDT for 1s

PORT    STATE    SERVICE     REASON      VERSION
139/tcp filtered netbios-ssn no-response

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 22:31:00 2025 -- 1 IP address (1 host up) scanned in 1.58 seconds
```

# enum4linux-ng

```
[92mENUM4LINUX - next generation (v1.3.4)[0m

 ==========================
|    Target Information    |
 ==========================
[94m[*] Target ........... 192.168.114.206[0m
[94m[*] Username ......... ''[0m
[94m[*] Random Username .. 'cyoiapze'[0m
[94m[*] Password ......... ''[0m
[94m[*] Timeout .......... 5 second(s)[0m

 ========================================
|    Listener Scan on 192.168.114.206    |
 ========================================
[94m[*] Checking LDAP[0m
[91m[-] Could not connect to LDAP on 389/tcp: timed out[0m
[94m[*] Checking LDAPS[0m
[91m[-] Could not connect to LDAPS on 636/tcp: timed out[0m
[94m[*] Checking SMB[0m
[92m[+] SMB is accessible on 445/tcp[0m
[94m[*] Checking SMB over NetBIOS[0m
[92m[+] SMB over NetBIOS is accessible on 139/tcp[0m

 ==============================================================
|    NetBIOS Names and Workgroup/Domain for 192.168.114.206    |
 ==============================================================
[V] Trying to get NetBIOS names information, running command: nmblookup -s /tmp/tmp23gw8xou -A 192.168.114.206
[91m[-] Could not get NetBIOS names information via 'nmblookup': timed out[0m

 ============================================
|    SMB Dialect Check on 192.168.114.206    |
 ============================================
[94m[*] Trying on 445/tcp[0m
[92m[+] Supported dialects and settings:
Supported dialects:
  SMB 1.0: false
  SMB 2.02: true
  SMB 2.1: true
  SMB 3.0: true
  SMB 3.1.1: true
Preferred dialect: SMB 3.0
SMB1 only: false
SMB signing required: false[0m

 ==============================================================
|    Domain Information via SMB session for 192.168.114.206    |
 ==============================================================
[94m[*] Enumerating via unauthenticated SMB session on 445/tcp[0m
[92m[+] Found domain information via SMB
NetBIOS computer name: WS26
NetBIOS domain name: OSCP
DNS domain: oscp.exam
FQDN: WS26.oscp.exam
Derived membership: domain member
Derived domain: OSCP[0m

 ============================================
|    RPC Session Check on 192.168.114.206    |
 ============================================
[94m[*] Check for null session[0m
[V] Attempting to make session, running command: smbclient -W OSCP -U % -s /tmp/tmp23gw8xou -t 5 -c help '//192.168.114.206/ipc$'
[91m[-] Could not establish null session: STATUS_ACCESS_DENIED[0m
[94m[*] Check for random user[0m
[V] Attempting to make session, running command: smbclient -W OSCP -U cyoiapze% -s /tmp/tmp23gw8xou -t 5 -c help '//192.168.114.206/ipc$'
[91m[-] Could not establish random user session: STATUS_LOGON_FAILURE[0m
[91m[-] Sessions failed, neither null nor user sessions were possible[0m

 ==================================================
|    OS Information via RPC for 192.168.114.206    |
 ==================================================
[94m[*] Enumerating via unauthenticated SMB session on 445/tcp[0m
[92m[+] Found OS information via SMB[0m
[94m[*] Enumerating via 'srvinfo'[0m
[91m[-] Skipping 'srvinfo' run, not possible with provided credentials[0m
[92m[+] After merging OS information we have the following result:
OS: Windows 10, Windows Server 2019, Windows Server 2016
OS version: '10.0'
OS release: ''
OS build: '22621'
Native OS: not supported
Native LAN manager: not supported
Platform id: null
Server type: null
Server type string: null[0m

[93m[!] Aborting remainder of tests since sessions failed, rerun with valid credentials[0m

Completed after 23.85 seconds


```

# smbclient

```
session setup failed: NT_STATUS_ACCESS_DENIED

```

# netexec 

```

```

# enumeration

## anon



## with credentials


