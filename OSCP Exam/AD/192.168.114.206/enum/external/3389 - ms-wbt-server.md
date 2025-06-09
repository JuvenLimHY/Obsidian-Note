# nmap 

```
# Nmap 7.95 scan initiated Sun Jun  8 22:30:59 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 3389 "--script=banner,(rdp* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp3389/tcp_3389_rdp_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.206/results/192.168.114.206/scans/tcp3389/xml/tcp_3389_rdp_nmap.xml 192.168.114.206
Nmap scan report for 192.168.114.206
Host is up, received user-set (0.24s latency).
Scanned at 2025-06-08 22:30:59 EDT for 56s

PORT     STATE SERVICE       REASON          VERSION
3389/tcp open  ms-wbt-server syn-ack ttl 127
|_ssl-date: TLS randomness does not represent time
| rdp-enum-encryption: 
|   Security layer
|     CredSSP (NLA): SUCCESS
|     CredSSP with Early User Auth: SUCCESS
|_    RDSTLS: SUCCESS
| rdp-ntlm-info: 
|   Target_Name: OSCP
|   NetBIOS_Domain_Name: OSCP
|   NetBIOS_Computer_Name: WS26
|   DNS_Domain_Name: oscp.exam
|   DNS_Computer_Name: WS26.oscp.exam
|   DNS_Tree_Name: oscp.exam
|   Product_Version: 10.0.22621
|_  System_Time: 2024-11-12T13:10:51+00:00
| ssl-enum-ciphers: 
|   TLSv1.0: 
|     ciphers: 
|       TLS_RSA_WITH_AES_256_CBC_SHA (rsa 2048) - A
|       TLS_RSA_WITH_AES_128_CBC_SHA (rsa 2048) - A
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA (secp384r1) - A
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (ecdh_x25519) - A
|     compressors: 
|       NULL
|     cipher preference: server
|   TLSv1.1: 
|     ciphers: 
|       TLS_RSA_WITH_AES_256_CBC_SHA (rsa 2048) - A
|       TLS_RSA_WITH_AES_128_CBC_SHA (rsa 2048) - A
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA (secp384r1) - A
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (ecdh_x25519) - A
|     compressors: 
|       NULL
|     cipher preference: server
|   TLSv1.2: 
|     ciphers: 
|       TLS_RSA_WITH_AES_256_GCM_SHA384 (rsa 2048) - A
|       TLS_RSA_WITH_AES_128_GCM_SHA256 (rsa 2048) - A
|       TLS_RSA_WITH_AES_256_CBC_SHA256 (rsa 2048) - A
|       TLS_RSA_WITH_AES_128_CBC_SHA256 (rsa 2048) - A
|       TLS_RSA_WITH_AES_256_CBC_SHA (rsa 2048) - A
|       TLS_RSA_WITH_AES_128_CBC_SHA (rsa 2048) - A
|       TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 (secp384r1) - A
|       TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 (ecdh_x25519) - A
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 (secp384r1) - A
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 (ecdh_x25519) - A
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA (secp384r1) - A
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (ecdh_x25519) - A
|     compressors: 
|       NULL
|     cipher preference: server
|   TLSv1.3: 
|     ciphers: 
|       TLS_AKE_WITH_AES_256_GCM_SHA384 (secp384r1) - A
|       TLS_AKE_WITH_AES_128_GCM_SHA256 (ecdh_x25519) - A
|     cipher preference: server
|_  least strength: A
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
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port3389-TCP:V=7.95%I=7%D=6/8%Time=68464770%P=x86_64-pc-linux-gnu%r(Ter
SF:minalServerCookie,13,"\x03\0\0\x13\x0e\xd0\0\0\x124\0\x02\?\x08\0\x02\0
SF:\0\0");

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 22:31:55 2025 -- 1 IP address (1 host up) scanned in 56.33 seconds

```
