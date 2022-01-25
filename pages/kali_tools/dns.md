### DNS

- DNS传输
    ```bash
        $ dig @ns4.sina.com.cn. sina.com axfr
        <<>> DiG 9.16.1-Ubuntu <<>> @ns4.sina.com.cn. sina.com axfr
        (1 server found)
        global options: +cmd
        Transfer failed.
        #失败了
        $ host -T -l sina.com ns4.sina.com.cn.
        Using domain server:
        Name: ns4.sina.com.cn.
        Address: 121.14.1.22#53
        Aliases: 
        Host sina.com not found: 5(REFUSED)
        ; Transfer failed.
        #同样失败了
    ```

_同上但是更加暴力_

- DNS字典爆破

    ```bash
    dnsdict6 -d4 -t 16 -u sina.com
    ```

- DNS注册信息

    ```bash
        whois 域名
    ```
- shodan搜索
    ```tips
        网址 www.shodan.com
        常见filter：
            net
            city
            country
            port
            os
            Hostname
            server
        200 ok cisco
        user:admin  pass:password
        linux upnp avtech
    ```
 