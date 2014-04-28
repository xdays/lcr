apt-cache
=====================================

简介
^^^^
包查询工具

选项
^^^^

* gencache 更新缓存
* showpkg 查看包信息
* stats 统计信息
* showsrc 源码包
* dump 查看所有包
* dumpavail 查看所有可用包
* show 类似dpkg --print-avial
* search 正则查询
* depends 包依赖
* rdepends 依赖该包的包
* pkgnames 打印包列表
* -a 所有版本
* -g 重新生成缓存

示例
^^^^

搜索python相关的包::

    apt-cache search python
