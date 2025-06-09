# nmap 

```
# Nmap 7.95 scan initiated Mon Jun  9 09:17:42 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 22 --script=banner,ssh2-enum-algos,ssh-hostkey,ssh-auth-methods -oN /home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/tcp22/tcp_22_ssh_nmap.txt -oX /home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/tcp22/xml/tcp_22_ssh_nmap.xml 192.168.114.110
Nmap scan report for 192.168.114.110
Host is up, received user-set (0.25s latency).
Scanned at 2025-06-09 09:17:42 EDT for 8s

PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 63 OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
|_banner: SSH-2.0-OpenSSH_8.9p1 Ubuntu-3ubuntu0.1
| ssh2-enum-algos: 
|   kex_algorithms: (10)
|       curve25519-sha256
|       curve25519-sha256@libssh.org
|       ecdh-sha2-nistp256
|       ecdh-sha2-nistp384
|       ecdh-sha2-nistp521
|       sntrup761x25519-sha512@openssh.com
|       diffie-hellman-group-exchange-sha256
|       diffie-hellman-group16-sha512
|       diffie-hellman-group18-sha512
|       diffie-hellman-group14-sha256
|   server_host_key_algorithms: (4)
|       rsa-sha2-512
|       rsa-sha2-256
|       ecdsa-sha2-nistp256
|       ssh-ed25519
|   encryption_algorithms: (6)
|       chacha20-poly1305@openssh.com
|       aes128-ctr
|       aes192-ctr
|       aes256-ctr
|       aes128-gcm@openssh.com
|       aes256-gcm@openssh.com
|   mac_algorithms: (10)
|       umac-64-etm@openssh.com
|       umac-128-etm@openssh.com
|       hmac-sha2-256-etm@openssh.com
|       hmac-sha2-512-etm@openssh.com
|       hmac-sha1-etm@openssh.com
|       umac-64@openssh.com
|       umac-128@openssh.com
|       hmac-sha2-256
|       hmac-sha2-512
|       hmac-sha1
|   compression_algorithms: (2)
|       none
|_      zlib@openssh.com
| ssh-hostkey: 
|   256 a7:09:ae:7c:78:41:c7:a8:b4:41:17:20:f5:cd:15:75 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBOr5uCXt89FpAjb9GOQNcVyLaq/OHs7gLBgEF+LvgxP2PeVbxGEW9AGyohwbVwrGZ2EGJasx7N6zdTFus9MoD7c=
|   256 6c:fc:3e:2e:95:6a:54:1e:98:89:0e:c9:97:69:10:b9 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIL4oFJ6o1QVPOR4nPRBBBfiiLKBrQ1TT/RswHqeNb9sP
| ssh-auth-methods: 
|   Supported authentication methods: 
|     publickey
|_    password
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 09:17:50 2025 -- 1 IP address (1 host up) scanned in 7.80 seconds

```

# ssh-audit

```

```