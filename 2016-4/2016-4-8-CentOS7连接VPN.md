1.安装

`sudo yum install ppp pptp pptp-setup`

2.新建连接

`sudo pptpsetup --create PPTP --server 98.126.34.74 --username jack --password 123`

3.开始连接

`sudo pppd call PPTP updetach`

如果出现

>LCP terminated by peer (MPPE required but peer refused)

修改

`sudo vi /etc/ppp/peers/PPTP`

在后面增加

`require-mppe-128`

连接成功会出现以下提示

>Using interface ppp0

>Connect: ppp0 <--> /dev/pts/2

>CHAP authentication succeeded

>MPPE 128-bit stateless compression enabled

>local  IP address 192.168.120.14

>remote IP address 192.168.120.1


4.检查是否连接上

`ifconfig`

出现`ppp0`说明已连接

5.将所有对外网络设置为通过ppp0

查看路由设置

`sudo route -n`

`sudo route add -net 0.0.0.0 dev ppp0`

![](http://7xqhly.com1.z0.glb.clouddn.com/Screenshot%20from%202016-04-08%2006:03:42.png)

关闭连接
`sudo killall pppd`




