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

        #只查a记录
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

    ```