dpkg
=====================================

简介
^^^^
debian底层包管理工具

选项
^^^^

* 包状态
    * not-installed 未安装
    * config-files 仅安装了配置文件
    * half-installed 半安装
    * unpacked 解压
    * half-configured 半配置
    * triggers-awaited  等待另一个包触发
    * triggers-pending 已经出发
    * installed 已安装

* 包选择状态
    * install 选中安装
    * hold 不被dpkg处理
    * deinstall 反安装，仅有配置文件
    * purge 完全卸载
* 包标志
    * reinst-required 重新安装

* 动作
    * -i 安装
    * --unpack 解包
    * --configure 配置
    * --triggers-only 仅处理trigger
    * -r 卸载
    * -P 完全卸载
    * dpkg-deb动作
        * -b 编译
        * -c 包内容
        * -e 控制信息
        * -x 解压文件
        * -X 解压并打印文件
        * -f 查看控制信息
        * -I 包信息
    * dpkg-query动作
        * -l 列出包
        * -s 状态
        * -L 列出包的文件
        * -S 通过文件来搜索对应的包
        * -P 查看包信息

* 选项
    * -R 递归式

示例
^^^^

查看一个文件属于哪个包::

    dpkg -S /path/filename
