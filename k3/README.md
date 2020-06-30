备份恢复cn.dat

1 管理员权限打开RoutAckProV1B2 ,防火墙允许通过，打开成功后关闭该软件即可。

2 管理员权限打开putty.exe ,防火墙允许通过，连接类型： telnet ，点“开始“

3 同样管理员权限打开tftpd64软件，允许防火墙通过，选择对应的电脑有线网卡

4 putty打开后的界面输入命令：cd /tmp; tftp -g -r K3_V21.5.37.246_tb.bin 192.168.2.104 回车，上传进度条完成后继续第5步。

注意，这里面的ipf地址要与tftpd中的地址要一致。不一致要改为相同可以了。

5 putty输入命令：cat K3_V21.5.37.246_tb.bin >/dev/mtdblock6 && reboot 回车，刷入固件，耐心等待几分钟，下面出现提示英文字样，机器自动重启就OK。

注意：各软件都以管理员权限打开，防火墙允许通过，命令中的IP地址要与ftftp中网卡的IP地址要一样，不一样要改相同。用不同的固件也要改成相同的名字。

curl -Lksf raw.githubusercontent.com/jokin1999/router_firmwares/master/k3/one|sh

欢迎加入刷机交流群：229140997
