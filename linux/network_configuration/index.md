# [Home](/)
# [../Home/Linux](../)
# Network Configuration
[Show Info](#show-info) 
<br/>  
[Set Info](#set-info)
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## Show Info
# 查看網絡接口和IP地址配置
```
ip addr
```
或者簡寫成
```
ip a
```
# 查看路由
```
ip route
```
或者簡寫成
```
ip r
```
# 查看網卡硬件信息
網卡速度和雙工模式
```
ethtool nic_name
```
網卡驅動信息
```
ethtool -i nic_name
```
## Set Info
# 設置IP
添加/刪除IP
```
ip addr add/del 192.168.0.1/24 dev nic_name
```
# 設置路由
添加/刪除默認路由
```
ip route add/del default via 192.168.0.1 dev nic_name
```
添加/刪除路由
```
ip route add/del 10.0.0.0/10 via 192.168.0.1 dev nic_name
```
# 設置DNS
直接修改 /etc/resolv.conf 文件
先備份再修改
```
cp /etc/resolv.conf /etc/resolv.conf.backup
vi /etc/resolv.conf
```
添加DNS地址
```
nameserver 8.8.8.8
```
不修改的話直接添加
```
echo "nameserver 8.8.8.8" | tee -a /etc/resolv.conf
```
tee 將輸出的内容保存到指定文件, -a 指append , -a在文件尾部添加内容, 如果不加 -a 的話文件會被内容覆蓋
