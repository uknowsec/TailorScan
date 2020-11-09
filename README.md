# TailorScan

```
 > TailorScan_windows_amd64.exe

ServerScan for Port Scaner and Service Version Detection.
HOST  Host to be scanned, supports four formats:
                192.168.1.1
                192.168.1.1-10
                192.168.1.*
                192.168.1.0/24
PORT  Customize port list, separate with ',' example: 21,22,80-99,8000-8080 ...
MODEL Scan Model: icmp or tcp
example: TailorScan.exe portscan 192.168.0.1/24 80,8080 tcp
example: TailorScan.exe portscan 192.168.0.1/24 tcp

EternalBlue scanner
example: TailorScan.exe ms17010 -i 192.168.0.1
example: TailorScan.exe ms17010 -n 192.168.0.1/24

OXID Find
example: TailorScan.exe oxidfind -i 192.168.0.1
example: TailorScan.exe oxidfind -n 192.168.0.1/24

ICMP check
example: TailorScan.exe icmpcheck 192.168.0.1/24
```
