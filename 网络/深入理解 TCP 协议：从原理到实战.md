## 网络工具

### telnet

1. 检查端口是否打开

   命令格式： telnet 域名或者ip 端口



### netstat:

列出所有套接字：netstat -a

只列出tcp套接字: netstat -at

只列出udp套接字: netstat -au

只列出处于监听状态的连接: netstat -l

列出处于监听状态的tcp连接: netstat -lt 

禁用端口映射: netstat -n

显示进程: netstat -ltnp

显示所有网卡信息：netstat -i



### tcpdump

查看数据包： tcpdump -i 网卡名 （any表示所有的网卡）

过滤主机： 在查看数据包的基础上加上host选项(这个是源地址，目的地址都可以)  	tcpdump -i any host ip

过滤源地址： tcpdump -i any src ip

过滤目的地址： tcpdump -i any dst ip

过滤端口： tcpdump -i any port portnumber

抓取80端口收到的包： tcpdump -i any dst port 80 

过滤端口范围内的流量： tcpdump portrange 21-23

禁用主机与端口解析：-n 与 -nn

过滤协议： tcpdump -i any -nn udp

用 ASCII 格式查看包体内容：-A 选项 

限制包大小：tcpdump -i any -nn port 80 -A -s 500 包大小限制在500（如果想显示包体所有内容，可以加上`-s 0`）





