### netcat 与 ncat

_Ubuntu系统(版本||系统不同 命令使用存在差异)，由于netcat无法使用机密方式进行连接，推荐使用ncat_
1. netcat
```bash
#监听端口
nc -lp yours_port
#通过TCP协议链接ip port 并显示详细信息
nc -nv ip yours_port
#主机端口扫描
nc -nvz ip yours_port [端口范围/单个端口]
#文件传输
S：nc -lp yours_port < demo.txt
C：nc -nv ip yours_port > demo.txt
# 其余操作
延时等待
-w times
传输完成关闭
-q times
```

1. nmap 中的 ncat工具
```bash
#使用基本一致，仅介绍ssh链接
ncat -nvl port --ssl
#分享shell
-c bash
```