apt-get
=====================================

简介
^^^^
debian高级包管理工具

选项
^^^^

* update 同步包索引
* upgrade 安装更新包
* dist-upgrade 版本升级
* dselect-upgrade 配合dselect的升级
* install 安装
* remove 卸载，但是配置保留
* purge 卸载，删除所有
* source 获取源码
* check 检查依赖性
* download 下载
* clean 清除下载的文件
* autoclean
* autoremove
* changelog 下载changelog
* -y 直接回答yes
* -c 指定配置文件

示例
^^^^

安装软件::

    apt-get install vim
