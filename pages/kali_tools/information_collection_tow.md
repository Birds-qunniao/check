### 主动信息收集

1. 使用代理，或僵尸主机
2. 使用choas掩盖流量

_二层_
- nmap
    ```bash
        #区域主机扫描
        nmap -sn 192.168.8.0/24
        nmap -iL ip_file -sn
    ```

_三层 icmp_

_四层 tcp //udp_
    ```bash
        #udp
        nmap 192.168.8.189 -PU80 -sn
        #tcp
        nmap 192.168.8.189 -PA80 -sn
        #ip
        nmap 192.168.8.189 -PO80 -sn
    ```
_端口_

_服务扫描_

```tip
    scapy很好用
```