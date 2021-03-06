##### 32位
`rpm -ivh http://dl.fedoraproject.org/pub/epel/6/i386/epel-release-6-8.noarch.rpm`
##### 64位
`rpm -ivh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm`

##### VirtualBox

```
yum install gcc 
yum install kernel
yum install kernel-devel 
yum install kernel-headers
reboot
chmod +x VirtualBox-4.3.4-91027-Linux_amd64.run
./VirtualBox-4.3.4-91027-Linux_amd64.run
```

##### VirtualBox虚拟器设置
1)系统 -> 主板 -> 启动顺序 -> 硬盘
2)声音 -> 启用声音(关)
3)网络 -> 网卡1 -> 连接方式 -> 桥接网卡
4)USB设备 -> 启用USB控制器

##### 复制虚拟电脑
重新初始化所有网卡的MAC地址

##### 指定IP
1) 查看设备(eth0 or eth1)
   `vi /etc/udev/rules.d/70-persistent-net.rules`
2) 修改连接
   `vi /etc/sysconfig/network-scripts/ifcfg-eth0`
> DEVICE=eth0    #见1)
> 
> GATEWAY=192.168.0.1      #具体的网关IP
> 
> IPADDR=192.168.0.200     #具体的IP
> 
> NETMASK=255.255.255.0
> 
> HWADDR=08:00:27:CB:D9:16 #具体的MAC地址
> 
> DNS1=211.95.1.97
> 
> DNS2=210.22.70.225
> 
> DNS1=211.95.72.1#中国联通
> 
> DNS1=202.96.209.5#中国联通
> 
> DNS1=202.96.209.6#中国电信
> 
> DNS1=202.96.209.133#中国电信
> 
> DNS1=202.96.209.134#中国电信 

3) service network restart

##### pac
`yum install http://softlayer-dal.dl.sourceforge.net/project/pacmanager/pac-4.0/pac-4.5.3.2-2.x86_64.rpm`

##### putty
`yum install putty`

##### openjdk
1)jre:
`yum install java-1.7.0-openjdk.x86_64`
2)jdk:
`yum install java-1.7.0-openjdk-devel.x86_64`
3)src
`yum install java-1.7.0-openjdk-src.x86_64`


##### filezilla
`yum install filezilla`

##### 远程桌面
`yum install tsclient`

##### git
`yum install git`

##### chrome
`yum install google-chrome-stable-27.0.1453.110-202711.x86_64.rpm`

##### skype
`yum install http://www.bromosapien.net:8080/others/skype-4.3.0.37-2.el6.i686.rpm`

##### vpn
`yum install pptp pptp-setup`

##### rar
###### x64版本
`wget http://www.rarlab.com/rar/rarlinux-x64-4.2.0.tar.gz`
###### x86版本
`wget http://www.rarlab.com/rar/rarlinux-4.2.0.tar.gz`

```
tar zxf rarlinux-x64-4.2.0.tar.gz
mv rar /usr/local/rar
cd /usr/local/rar
make
```
