cp
=====================================

简介
^^^^
拷贝文件或者目录

选项
^^^^

* -a 等同于-dR
* --attributes-only 仅拷贝属性
* --backup/-b 备份目标文件
* --copy-contents 仅拷贝内容
* -d 保留链接属性
* -f 如果目标文件存在无法打开就删除后重新拷贝
* -i 交互式操作
* -H 跟踪链接
* -l 创建硬链接
* -n 不覆盖存在的文件
* -P 同-d
* -p 保留属性
* --preserve 保留指定属性
* --no-preserve 不保留指定属性
* --parents 使用绝对路径
* -R/r 递归式拷贝
* --remove-destination 先删除后打开文件
* -s 创建软链接

示例
^^^^

拷贝文件::

    cp -ap src dest
