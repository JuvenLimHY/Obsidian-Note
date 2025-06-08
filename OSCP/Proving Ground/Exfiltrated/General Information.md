# Host information

```
192.168.143.163
```

# Scans

# Curl
```
┌──(kali㉿kali)-[~/OSCP/pg/exfiltrated]
└─$ curl -v  http://192.168.143.163
*   Trying 192.168.143.163:80...
* Connected to 192.168.143.163 (192.168.143.163) port 80
* using HTTP/1.x
> GET / HTTP/1.1
> Host: 192.168.143.163
> User-Agent: curl/8.13.0
> Accept: */*
> 
* Request completely sent off
< HTTP/1.1 302 Found
< Date: Sun, 08 Jun 2025 06:55:00 GMT
< Server: Apache/2.4.41 (Ubuntu)
< Set-Cookie: INTELLI_06c8042c3d=0of20f64eu776d4jefu6l516l1; path=/
< Expires: Thu, 19 Nov 1981 08:52:00 GMT
< Cache-Control: no-store, no-cache, must-revalidate
< Pragma: no-cache
< Set-Cookie: INTELLI_06c8042c3d=0of20f64eu776d4jefu6l516l1; expires=Sun, 08-Jun-2025 07:25:00 GMT; Max-Age=1800; path=/
< Location: http://exfiltrated.offsec/
< Content-Length: 0
< Content-Type: text/html; charset=UTF-8
< 

```
## nmap

### quick scan

```
# Nmap 7.95 scan initiated Sun Jun  8 04:24:32 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/_quick_tcp_nmap.txt -oX /home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/xml/_quick_tcp_nmap.xml 192.168.143.163
adjust_timeouts2: packet supposedly had rtt of -675959 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -675959 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -452848 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -452848 microseconds.  Ignoring time.
Nmap scan report for exfiltrated.offsec (192.168.143.163)
Host is up, received user-set (0.020s latency).
Scanned at 2025-06-08 04:24:32 EDT for 16s
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 61 OpenSSH 8.2p1 Ubuntu 4ubuntu0.2 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 c1:99:4b:95:22:25:ed:0f:85:20:d3:63:b4:48:bb:cf (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDH6PH1/ST7TUJ4Mp/l4c7G+TM07YbX7YIsnHzq1TRpvtiBh8MQuFkL1SWW9+za+h6ZraqoZ0ewwkH+0la436t9Q+2H/Nh4CntJOrRbpLJKg4hChjgCHd5KiLCOKHhXPs/FA3mm0Zkzw1tVJLPR6RTbIkkbQiV2Zk3u8oamV5srWIJeYUY5O2XXmTnKENfrPXeHup1+3wBOkTO4Mu17wBSw6yvXyj+lleKjQ6Hnje7KozW5q4U6ijd3LmvHE34UHq/qUbCUbiwY06N2Mj0NQiZqWW8z48eTzGsuh6u1SfGIDnCCq3sWm37Y5LIUvqAFyIEJZVsC/UyrJDPBE+YIODNbN2QLD9JeBr8P4n1rkMaXbsHGywFtutdSrBZwYuRuB2W0GjIEWD/J7lxKIJ9UxRq0UxWWkZ8s3SNqUq2enfPwQt399nigtUerccskdyUD0oRKqVnhZCjEYfX3qOnlAqejr3Lpm8nA31pp6lrKNAmQEjdSO8Jxk04OR2JBxcfVNfs=
|   256 0f:44:8b:ad:ad:95:b8:22:6a:f0:36:ac:19:d0:0e:f3 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBI0EdIHR7NOReMM0G7C8zxbLgwB3ump+nb2D3Pe3tXqp/6jNJ/GbU2e4Ab44njMKHJbm/PzrtYzojMjGDuBlQCg=
|   256 32:e1:2a:6c:cc:7c:e6:3e:23:f4:80:8d:33:ce:9b:3a (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIDCc0saExmeDXtqm5FS+D5RnDke8aJEvFq3DJIr0KZML
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.41 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-title: Home :: Powered by Subrion 4.2
|_http-favicon: Unknown favicon MD5: 09BDDB30D6AE11E854BFF82ED638542B
| http-robots.txt: 7 disallowed entries 
| /backup/ /cron/? /front/ /install/ /panel/ /tmp/ 
|_/updates/
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-generator: Subrion CMS - Open Source Content Management System
Device type: general purpose|router|firewall
Running (JUST GUESSING): Linux 5.X|4.X|2.6.X|3.X (93%), MikroTik RouterOS 7.X (93%), IPFire 2.X (86%)
OS CPE: cpe:/o:linux:linux_kernel:5 cpe:/o:mikrotik:routeros:7 cpe:/o:linux:linux_kernel:5.6.3 cpe:/o:linux:linux_kernel:4 cpe:/o:linux:linux_kernel:2.6 cpe:/o:linux:linux_kernel:3 cpe:/o:ipfire:ipfire:2.27 cpe:/o:linux:linux_kernel:6.1
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 5.0 - 5.14 (93%), MikroTik RouterOS 7.2 - 7.5 (Linux 5.6.3) (93%), Linux 4.19 - 5.15 (92%), Linux 4.15 - 5.19 (90%), Linux 2.6.32 - 3.13 (89%), Linux 3.10 - 4.11 (89%), Linux 4.15 (88%), Linux 5.0 (87%), OpenWrt 22.03 (Linux 5.10) (87%), Linux 2.6.32 (87%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/8%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=684548D0%P=x86_64-pc-linux-gnu)
SEQ(SP=100%GCD=1%ISR=109%TI=Z%TS=A)
SEQ(SP=104%GCD=1%ISR=10D%TI=Z%II=I%TS=A)
OPS(O1=M578ST11NW7%O2=M578ST11NW7%O3=M578NNT11NW7%O4=M578ST11NW7%O5=M578ST11NW7%O6=M578ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M578NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=Y%DF=Y%TG=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 43.600 days (since Fri Apr 25 14:00:31 2025)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 1720/tcp)
HOP RTT      ADDRESS
1   33.60 ms 192.168.45.1
2   33.47 ms 192.168.45.254
3   33.99 ms 192.168.251.1
4   33.99 ms exfiltrated.offsec (192.168.143.163)

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 04:24:48 2025 -- 1 IP address (1 host up) scanned in 16.05 seconds

```
### full scan 

```
# Nmap 7.95 scan initiated Sun Jun  8 04:24:32 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/_full_tcp_nmap.txt -oX /home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/xml/_full_tcp_nmap.xml 192.168.143.163
adjust_timeouts2: packet supposedly had rtt of -345020 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -345020 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -460256 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -460256 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -486030 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -486030 microseconds.  Ignoring time.
Nmap scan report for exfiltrated.offsec (192.168.143.163)
Host is up, received user-set (0.045s latency).
Scanned at 2025-06-08 04:24:32 EDT for 30s
Not shown: 65533 closed tcp ports (reset)

PORT   STATE SERVICE REASON         VERSION

22/tcp open  ssh     syn-ack ttl 61 OpenSSH 8.2p1 Ubuntu 4ubuntu0.2 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 c1:99:4b:95:22:25:ed:0f:85:20:d3:63:b4:48:bb:cf (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDH6PH1/ST7TUJ4Mp/l4c7G+TM07YbX7YIsnHzq1TRpvtiBh8MQuFkL1SWW9+za+h6ZraqoZ0ewwkH+0la436t9Q+2H/Nh4CntJOrRbpLJKg4hChjgCHd5KiLCOKHhXPs/FA3mm0Zkzw1tVJLPR6RTbIkkbQiV2Zk3u8oamV5srWIJeYUY5O2XXmTnKENfrPXeHup1+3wBOkTO4Mu17wBSw6yvXyj+lleKjQ6Hnje7KozW5q4U6ijd3LmvHE34UHq/qUbCUbiwY06N2Mj0NQiZqWW8z48eTzGsuh6u1SfGIDnCCq3sWm37Y5LIUvqAFyIEJZVsC/UyrJDPBE+YIODNbN2QLD9JeBr8P4n1rkMaXbsHGywFtutdSrBZwYuRuB2W0GjIEWD/J7lxKIJ9UxRq0UxWWkZ8s3SNqUq2enfPwQt399nigtUerccskdyUD0oRKqVnhZCjEYfX3qOnlAqejr3Lpm8nA31pp6lrKNAmQEjdSO8Jxk04OR2JBxcfVNfs=
|   256 0f:44:8b:ad:ad:95:b8:22:6a:f0:36:ac:19:d0:0e:f3 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBI0EdIHR7NOReMM0G7C8zxbLgwB3ump+nb2D3Pe3tXqp/6jNJ/GbU2e4Ab44njMKHJbm/PzrtYzojMjGDuBlQCg=
|   256 32:e1:2a:6c:cc:7c:e6:3e:23:f4:80:8d:33:ce:9b:3a (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIDCc0saExmeDXtqm5FS+D5RnDke8aJEvFq3DJIr0KZML

80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.41 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-robots.txt: 7 disallowed entries 
| /backup/ /cron/? /front/ /install/ /panel/ /tmp/ 
|_/updates/
|_http-title: Home :: Powered by Subrion 4.2
|_http-generator: Subrion CMS - Open Source Content Management System
|_http-favicon: Unknown favicon MD5: 09BDDB30D6AE11E854BFF82ED638542B
|_http-server-header: Apache/2.4.41 (Ubuntu)
Device type: general purpose|router|storage-misc
Running (JUST GUESSING): Linux 5.X|4.X|2.6.X|3.X (98%), MikroTik RouterOS 7.X (97%), HP embedded (89%)
OS CPE: cpe:/o:linux:linux_kernel:5 cpe:/o:mikrotik:routeros:7 cpe:/o:linux:linux_kernel:5.6.3 cpe:/o:linux:linux_kernel:4 cpe:/o:linux:linux_kernel:2.6 cpe:/o:linux:linux_kernel:3 cpe:/h:hp:p2000_g3
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 5.0 - 5.14 (98%), MikroTik RouterOS 7.2 - 7.5 (Linux 5.6.3) (97%), Linux 4.15 - 5.19 (94%), Linux 2.6.32 - 3.13 (93%), OpenWrt 22.03 (Linux 5.10) (92%), Linux 5.0 (91%), Linux 3.10 - 4.11 (90%), Linux 3.2 - 4.14 (90%), Linux 2.6.32 - 3.10 (90%), Linux 4.15 (89%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/8%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=684548DE%P=x86_64-pc-linux-gnu)
SEQ(SP=105%GCD=1%ISR=10B%TI=Z%CI=Z%II=I%TS=A)
SEQ(SP=F6%GCD=1%ISR=106%TI=Z%CI=Z%II=I%TS=A)
OPS(O1=M578ST11NW7%O2=M578ST11NW7%O3=M578NNT11NW7%O4=M578ST11NW7%O5=M578ST11NW7%O6=M578ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M578NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=Y%DF=Y%TG=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=Y%DF=Y%TG=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)
T7(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 43.600 days (since Fri Apr 25 14:00:32 2025)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=261 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 3389/tcp)
HOP RTT      ADDRESS
1   69.32 ms 192.168.45.1
2   69.31 ms 192.168.45.254
3   74.80 ms 192.168.251.1
4   74.85 ms exfiltrated.offsec (192.168.143.163)

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 04:25:02 2025 -- 1 IP address (1 host up) scanned in 30.19 seconds

```
### udp scan

```
# Nmap 7.95 scan initiated Sun Jun  8 04:24:32 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/_top_100_udp_nmap.txt -oX /home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/xml/_top_100_udp_nmap.xml 192.168.143.163
Increasing send delay for 192.168.143.163 from 50 to 100 due to 11 out of 15 dropped probes since last increase.
Increasing send delay for 192.168.143.163 from 100 to 200 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for 192.168.143.163 from 400 to 800 due to 11 out of 11 dropped probes since last increase.
Nmap scan report for exfiltrated.offsec (192.168.143.163)
Host is up, received user-set (0.027s latency).
Scanned at 2025-06-08 04:24:32 EDT for 344s

PORT      STATE         SERVICE         REASON              VERSION
7/udp     closed        echo            port-unreach ttl 61
9/udp     closed        discard         port-unreach ttl 61
17/udp    closed        qotd            port-unreach ttl 61
19/udp    closed        chargen         port-unreach ttl 61
49/udp    closed        tacacs          port-unreach ttl 61
53/udp    open|filtered domain          no-response
67/udp    open|filtered dhcps           no-response
68/udp    open|filtered dhcpc           no-response
69/udp    closed        tftp            port-unreach ttl 61
80/udp    closed        http            port-unreach ttl 61
88/udp    open|filtered kerberos-sec    no-response
111/udp   closed        rpcbind         port-unreach ttl 61
120/udp   closed        cfdptkt         port-unreach ttl 61
123/udp   closed        ntp             port-unreach ttl 61
135/udp   open|filtered msrpc           no-response
136/udp   closed        profile         port-unreach ttl 61
137/udp   open|filtered netbios-ns      no-response
138/udp   open|filtered netbios-dgm     no-response
139/udp   closed        netbios-ssn     port-unreach ttl 61
158/udp   closed        pcmail-srv      port-unreach ttl 61
161/udp   closed        snmp            port-unreach ttl 61
162/udp   closed        snmptrap        port-unreach ttl 61
177/udp   open|filtered xdmcp           no-response
427/udp   open|filtered svrloc          no-response
443/udp   open|filtered https           no-response
445/udp   closed        microsoft-ds    port-unreach ttl 61
497/udp   closed        retrospect      port-unreach ttl 61
500/udp   closed        isakmp          port-unreach ttl 61
514/udp   open|filtered syslog          no-response
515/udp   closed        printer         port-unreach ttl 61
518/udp   open|filtered ntalk           no-response
520/udp   closed        route           port-unreach ttl 61
593/udp   open|filtered http-rpc-epmap  no-response
623/udp   closed        asf-rmcp        port-unreach ttl 61
626/udp   open|filtered serialnumberd   no-response
631/udp   open|filtered ipp             no-response
996/udp   closed        vsinet          port-unreach ttl 61
997/udp   closed        maitrd          port-unreach ttl 61
998/udp   closed        puparp          port-unreach ttl 61
999/udp   open|filtered applix          no-response
1022/udp  closed        exp2            port-unreach ttl 61
1023/udp  open|filtered unknown         no-response
1025/udp  open|filtered blackjack       no-response
1026/udp  open|filtered win-rpc         no-response
1027/udp  closed        unknown         port-unreach ttl 61
1028/udp  open|filtered ms-lsa          no-response
1029/udp  closed        solid-mux       port-unreach ttl 61
1030/udp  open|filtered iad1            no-response
1433/udp  closed        ms-sql-s        port-unreach ttl 61
1434/udp  open|filtered ms-sql-m        no-response
1645/udp  closed        radius          port-unreach ttl 61
1646/udp  open|filtered radacct         no-response
1701/udp  closed        L2TP            port-unreach ttl 61
1718/udp  open|filtered h225gatedisc    no-response
1719/udp  closed        h323gatestat    port-unreach ttl 61
1812/udp  closed        radius          port-unreach ttl 61
1813/udp  closed        radacct         port-unreach ttl 61
1900/udp  open|filtered upnp            no-response
2000/udp  open|filtered cisco-sccp      no-response
2048/udp  closed        dls-monitor     port-unreach ttl 61
2049/udp  closed        nfs             port-unreach ttl 61
2222/udp  open|filtered msantipiracy    no-response
2223/udp  open|filtered rockwell-csp2   no-response
3283/udp  open|filtered netassistant    no-response
3456/udp  open|filtered IISrpc-or-vat   no-response
3703/udp  open|filtered adobeserver-3   no-response
4444/udp  closed        krb524          port-unreach ttl 61
4500/udp  closed        nat-t-ike       port-unreach ttl 61
5000/udp  closed        upnp            port-unreach ttl 61
5060/udp  open|filtered sip             no-response
5353/udp  closed        zeroconf        port-unreach ttl 61
5632/udp  open|filtered pcanywherestat  no-response
9200/udp  closed        wap-wsp         port-unreach ttl 61
10000/udp open|filtered ndmp            no-response
17185/udp open|filtered wdbrpc          no-response
20031/udp closed        bakbonenetvault port-unreach ttl 61
30718/udp closed        unknown         port-unreach ttl 61
31337/udp open|filtered BackOrifice     no-response
32768/udp open|filtered omad            no-response
32769/udp closed        filenet-rpc     port-unreach ttl 61
32771/udp closed        sometimes-rpc6  port-unreach ttl 61
32815/udp open|filtered unknown         no-response
33281/udp closed        unknown         port-unreach ttl 61
49152/udp open|filtered unknown         no-response
49153/udp closed        unknown         port-unreach ttl 61
49154/udp closed        unknown         port-unreach ttl 61
49156/udp open|filtered unknown         no-response
49181/udp closed        unknown         port-unreach ttl 61
49182/udp open|filtered unknown         no-response
49185/udp open|filtered unknown         no-response
49186/udp open|filtered unknown         no-response
49188/udp open|filtered unknown         no-response
49190/udp open|filtered unknown         no-response
49191/udp open|filtered unknown         no-response
49192/udp closed        unknown         port-unreach ttl 61
49193/udp closed        unknown         port-unreach ttl 61
49194/udp closed        unknown         port-unreach ttl 61
49200/udp open|filtered unknown         no-response
49201/udp open|filtered unknown         no-response
65024/udp open|filtered unknown         no-response
Too many fingerprints match this host to give specific OS details
TCP/IP fingerprint:
SCAN(V=7.95%E=4%D=6/8%OT=%CT=%CU=7%PV=Y%DS=4%DC=T%G=N%TM=68454A18%P=x86_64-pc-linux-gnu)
SEQ(CI=Z%II=I)
T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)
U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)
IE(R=Y%DFI=N%T=40%CD=S)

Network Distance: 4 hops

TRACEROUTE (using port 33281/udp)
HOP RTT     ADDRESS
1   7.71 ms 192.168.45.1
2   7.72 ms 192.168.45.254
3   7.72 ms 192.168.251.1
4   7.75 ms exfiltrated.offsec (192.168.143.163)

Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 04:30:16 2025 -- 1 IP address (1 host up) scanned in 343.47 seconds

```

## rustscan

```
┌──(kali㉿kali)-[~/Downloads]
└─$ rustscan -a 192.168.143.163
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
0day was here ♥

[~] The config file is expected to be at "/home/kali/.rustscan.toml"
[!] File limit is lower than default batch size. Consider upping with --ulimit. May cause harm to sensitive servers
[!] Your file limit is very small, which negatively impacts RustScan's speed. Use the Docker image, or up the Ulimit with '--ulimit 5000'. 
Open 192.168.143.163:22
Open 192.168.143.163:80
[~] Starting Script(s)
[~] Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-08 05:23 EDT
Initiating Ping Scan at 05:23
Scanning 192.168.143.163 [4 ports]
Completed Ping Scan at 05:23, 0.05s elapsed (1 total hosts)
Initiating SYN Stealth Scan at 05:23
Scanning exfiltrated.offsec (192.168.143.163) [2 ports]
Discovered open port 22/tcp on 192.168.143.163
Discovered open port 80/tcp on 192.168.143.163
Completed SYN Stealth Scan at 05:23, 0.07s elapsed (2 total ports)
Nmap scan report for exfiltrated.offsec (192.168.143.163)
Host is up, received reset ttl 61 (0.019s latency).
Scanned at 2025-06-08 05:23:24 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack ttl 61
80/tcp open  http    syn-ack ttl 61

Read data files from: /usr/share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.24 seconds
           Raw packets sent: 6 (240B) | Rcvd: 3 (128B)

```