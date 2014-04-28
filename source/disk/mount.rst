mount
=====================================

简介
^^^^
挂载一个文件系统

选项
^^^^

* -v 打印过程信息
* -a 挂在fstab下的所有文件系统
* -F 每个挂在点开启一个子进程
* -f 执行但是不调用系统调用
* -l 添加卷标
* -n 挂载但是不写入mtab文件
* -s 忽略文件系统不支持的选项
* -r 以只读形式挂载文件系统，等同-o ro
* -w 以读写形式挂在，等同于-o rw
* -L 以卷标识别设备
* -U 以UUID识别设备
* -t 文件系统类型
* -o 指定以逗号分割的文件系统参数
* -B 以bind方式挂载
* -R 递归式挂载
* -M 移动式挂载
* fstab文件支持的选项
    * sync/async 同步/异步更新
    * atime/noatime 是否记录访问时间
    * auto/noauto -a时是否自动挂载
    * default 默认选项，包括rw, suid, dev, exec, auto, nouser, and async
    * diratime/nodiratime 是否记录目录访问时间
    * exec/noexec 是否允许执行二进制文件
    * suid/nosuid 是否允许suid标志
    * owner 允许设备所有者挂载
    * remount 重新挂载
    * ro 只读
    * rw 读写
    * user/users/nouser 是否允许普通用户挂载

示例
^^^^

挂载磁盘::

    mount -t ext3 /dev/sda1 /mnt/
