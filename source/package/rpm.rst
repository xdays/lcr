rpm
=====================================

简介
^^^^
redhat包管理工具

选项
^^^^

* 查询
    * -q 根据包名查询
    * -V 验证
    * --changelog 查changelog
    * -c 配置文件
    * -d 文档文件
    * -i 包信息
    * -l 文件列表
    * -f 查询文件所属包

* 安装
    * -i 安装
    * --force 强制安装
    * --nodigest 不校验报头digest
    * --nodeps 不解决依赖
    * -U 升级
    * -F 刷新
    * -e 卸载

* 杂项
    * --initdb/rebuilddb 初始化数据库
    * --addsign 签名
    * --showrc rpm环境变量

* 选择
    * -a 所有
    * -g 组
    * -p 包文件


示例
^^^^

查询包包含的文件::

    rpm -ql vsftp

查询文件所属包::

    rpm -qf /etc/vsftpd/vsftpd.conf
