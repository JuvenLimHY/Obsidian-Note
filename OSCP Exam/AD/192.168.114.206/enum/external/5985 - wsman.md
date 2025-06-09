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

can do anything as user got no permission, script is disabled for this system, maybe winpeas might work=