### 信息收集

_nslookup用于域名解析_

- nslookup
  
    ```bash
        $ nslookup
        > www.google.com
        Server:		127.0.0.53
        Address:	127.0.0.53#53

        Non-authoritative answer:
        Name:	www.google.com
        Address: 157.240.10.32

        #只查a(主机)记录
        > set type=a
        > www.sina.com
        Server:		127.0.0.53
        Address:	127.0.0.53#53

        Non-authoritative answer:
        www.sina.com	canonical name = spool.grid.sinaedge.com.
        Name:	spool.grid.sinaedge.com
        Address: 120.192.83.103
        Name:	spool.grid.sinaedge.com
        Address: 120.192.83.98
        # 查询域名解析服务器
        > set type=ns
        > sina.com
        Server:		127.0.0.53
        Address:	127.0.0.53#53

        Non-authoritative answer:
        sina.com	nameserver = ns4.sina.com.cn.
        sina.com	nameserver = ns3.sina.com.
        sina.com	nameserver = ns3.sina.com.cn.
        sina.com	nameserver = ns1.sina.com.
        sina.com	nameserver = ns2.sina.com.
        sina.com	nameserver = ns4.sina.com.
        sina.com	nameserver = ns1.sina.com.cn.
        sina.com	nameserver = ns2.sina.com.cn.

        #根据ip反解析域名
        > set q=ptr
        > 157.240.10.32
        Server:		127.0.0.53
        Address:	127.0.0.53#53

        Non-authoritative answer:
        32.10.240.157.in-addr.arpa	name = edge-mqtt-mini-shv-01-kut2.facebook.com.

        Authoritative answers can be found from:
        #通过域名反解析主机
        > set q=a
        > google.com
        Server:		127.0.0.53
        Address:	127.0.0.53#53

        Non-authoritative answer:
        Name:	google.com
        Address: 172.217.163.46
    ```
_dig 增强型nslookup_

- dig
  
    ```bash
        dig google.com any @8.8.8.8
        # 反响解析 参数 -x
        dig +trace sina.com
    ```