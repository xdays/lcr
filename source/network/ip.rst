ip
=====================================

简介
^^^^
查看和修改路由表，设备信息，策略路由和隧道

选项
^^^^

* 对象

    * address 地址
    * addrlabel 协议标配置
    * l2tp 基于IP的隧道以太网
    * link 设备
    * maddress 组播
    * monitor 监控
    * mroute 组播路由
    * mrule 组播路由策略
    * neighbour ARP
    * netns 网络名字空间
    * ntable 邻居
    * route 路由
    * rule 路由策略
    * tcp_metrics/tcpmetrics TCP的metric
    * tunnel 基于IP的对道
    * tuntap tap设备
    * xfrm IPSec的策略

* 操作

    * add 增加
    * del 删除
    * show/list 查看
    * help 帮助

示例
^^^^

::

    ip addr show
