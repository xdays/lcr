iptables
=====================================

简介
^^^^
IPv4包过滤和NAT管理工具

选项
^^^^

* 表

    * filter 过滤
    * nat 地址转换
    * mangle 修改数据包
    * raw 追踪
    * security 和SELinux相关

* 选项

    * 命令

        * -A 追加
        * -C 检查是否存在
        * -D 删除
        * -I 插入
        * -R 替换
        * -L 列举
        * -S 输出所有规则
        * -F 清空表
        * -Z 清空计数器
        * -N 新建自定义链
        * -X 删除自定义链
        * -P 设置默认规则
        * -E 重命名链

    * 匹配规则

        * -4 ipv4
        * -6 ipv6
        * -p 协议
        * -s 源IP
        * -d 目的IP
        * -m 指定匹配
        * -j 目标动作
        * -g 跳转到指定链
        * -i 数据包流入接口
        * -o 数据包流出接口
        * -f 分片数据包
        * -c 设置计数器

    * 其他选项

        * -n 数字输出
        * -x 准确的转换
        * --line-numbers
        * --modprobe= 挂载模块

* 扩展匹配规则

    *  `参考文档 http://www.web-manual.net/linux-3/the-kernel-ring-buffer-and-dmesg/`_

* 目标

    * ACCEPT 接受
    * DROP 丢弃
    * QUEUE 进入用户空间
    * RETURN 跳过当前链

* 扩展目标

    * DNAT 目的地址转换

        * --to-destination ip:port 指给指定设备和端口

    * LOG 写日志
    * MASQUERADE 用于nat表的POSTROUTING链，用于动态的SNAT
    * SNAT 用于nat表的POSTROUTING链

        * --to-source ip:port 指定修改的地址和端口

    *  `参考文档 http://www.web-manual.net/linux-3/the-kernel-ring-buffer-and-dmesg/`_

示例
^^^^

::

    iptables -t nat -A POSTROUTING  -s 192.168.110.0/24 -j MASQUERADE
