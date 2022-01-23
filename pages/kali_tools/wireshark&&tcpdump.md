### netcat 与 ncat

_Wireshark 主要用于网络抓包及其分析，相关计算机网络信息请自行补充_

- Wireshark
    1. 选择网络接口
    ![image](../../images/Kalitools/2022-01-21-wireshark.png 'wireshark')
    1. 开始捕获数据包
    - 第一层Frame 为数据包信息
    ![image](../../images/Kalitools/2022-01-22-bluetooth.png 'wireshark')
    - 第二层为以太网包头信息，二层上层协议类型
    ![image](../../images/Kalitools/2022-01-22.png 'wireshark')
    - 第三层为协议包头，及其信息,三层上层协议
    - 第四层为具体协议包头信息

- Tcpdump

    _Tcpdump 不添加任何参数的话，仅抓取64位的文件_
    - 抓取
        ```bash
            tcpdump -i 网卡名称  port 端口号 -s 抓取文件大小 -w 写入文件.pcap
            # tcp port 端口号  仅抓取tcp包
            # tcpdump 读取文件
            tcpdump -r 文件.pcap
            # -A 以accic码显示
            # -x 以16进制显示
        ```
    - 筛选
        ```bash
            #不解析ip域名读取文件
            tcpdump -n -r 文件.pcap
            tcpdump -n src host ip -r pcap文件
             
        ```
        _高级筛选请 man tcpdump_
```bash
#Tip 文件转base64命令
    base64 文件路径 > base64_code_file
```