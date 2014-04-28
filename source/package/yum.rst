yum
=====================================

简介
^^^^
类似apt-get的包管理工具

选项
^^^^

* install 安装
* update 更新
* upgrade 升级
* remove 删除
* list 查看所有信息
* info 描述信息
* provides 搜索哪些包提供对应功能和文件
* clean 清理缓存
* makecache 更新缓存
* groupinstall 组安装
* groupupdate 组更新
* grouplist 组列表
* groupremove 组删除
* groupinfo 组信息
* search 搜索
* shell 进入yum shell
* localinstall 本地安装
* localupdate 本地更新
* reinstall 重新安装
* downgrade 降版本
* deplist 依赖列表
* repolist 源列表
* version 版本
* check 检查数据库
* -y 默认yes
* --enablerepo= 开启源
* --nogpgcheck 不检查gpg签名

示例
^^^^

安装包::

    yum install vim

查询文件所属包::

    yum provide /usr/bin/vim
