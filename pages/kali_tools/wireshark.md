### netcat 与 ncat

_Wireshark 主要用于网络抓包及其分析，相关计算机网络信息请自行补充_

1. 选择网络接口
![image](../../images/Kalitools/2022-01-21-wireshark.png 'wireshark')
2. 开始捕获数据包
 - 第一层Frame 为数据包信息
![image](../../images/Kalitools/2022-01-22-bluetooth.png 'wireshark')
 - 第二层为以太网包头信息，二层上层协议类型
![image](../../images/Kalitools/2022-01-22-network.png 'wireshark')
 - 第三层为协议包头，及其信息,三层上层协议
 - 第四层为具体协议包头信息
```bash
#Tip 文件转base64命令
    base64 文件路径 > base64_code_file
```