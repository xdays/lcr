ifconfig
=====================================

简介
^^^^
配置网络接口

选项
^^^^

* -a 查看所有接口
* -s 输出简短列表
* interface 支持子接口
* up/down 开关接口
* [-]arp 开关arp协议
* [-]promisc 开关混杂模式
* [-]allmulti 开关广播模式，收所有的包
* metric metric值
* mtu 最大传输单元
* netmask 掩码
* add/del 添加删除ipv6地址
* tunnel 创建v6-v4的隧道
* irq 中断号
* io_addr IO地址
* media 介质类型10/100M
* [-]broadcast 开关广播地址
* [-]pointopoint 配置点对点地址
* hw 物理地址
* multicast 组播
* address IP地址
* txqueuelen 传输队列

示例
^^^^

::

    ifconfig eth0:0 192.168.1.1 netmask 255.255.255.0
