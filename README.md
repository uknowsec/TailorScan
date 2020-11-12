## TailorScan


扫描是内网渗透的一个主要组成部分，自认为，在内网中CLI与GUI更偏向于CLI。更适用于webshell，CobaltStrike等一些C2工具。同时在编程语言方面，Go更为合适，交叉编译支持多平台兼容性好相较于Python和C#，开发难度较小相较于C/C++。个人需求，在内网更多的是端口扫描，探测存活和ms17010检测这几部分的需求比较多。

秉着不重复造轮子和能用就行的原则，发现github上的[ServerScan](https://github.com/Adminisme/ServerScan)满足我在端口扫描上的需求。下面是GitHub给出的介绍

- 多平台支持（Windows、Mac、Linux、Cobalt Strike）
- 存活IP探测（支持TCP、ICMP两种模式）
- 超快的端口扫描
- 服务和应用版本检测功能，内置指纹探针采用:[nmap-service-probes](https://raw.githubusercontent.com/nmap/nmap/master/nmap-service-probes)
- Web服务（http、https）信息探测

简单就是多平台支持，可识别服务和应用，可获取title。

起初只是用他进行一些内网的端口扫描，后续因为项目开源，开始在上面加了一些自己常用的功能，例如上面提到的探测网卡，ms17010功能。就有了这个TailorScan（缝合怪扫描器）。再内置了自己常用的一些端口，在内网渗透中还是挺好用的。

#### Usage

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

### References

https://github.com/Adminisme/ServerScan
