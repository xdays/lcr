sysctl
=====================================

简介
^^^^
实时配置内核参数

选项
^^^^

* variable 读取key
* variable=value 设置key
* -n 只打印值
* -e 忽略错误信息
* -N 仅打印名字
* -q 静默模式
* -w 写入配置文件
* -p/-f 从文件中读取
* -a/-x/-A 打印所有的设置值
* -b 输出时不换行
* --system 读取系统配置
* --pattern 模式匹配
*

示例
^^^^

::

    sysctl -a --pattern 'net.ipv4.conf.(eth|wlan)0.arp'
