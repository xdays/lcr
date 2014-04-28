modprobe
=====================================

简介
^^^^
增删内核模块

选项
^^^^

* -a 安装所有模块
* -C 指定配置文件
* -c 解析配置文件
* --dump-modversions 模块版本信息
* -d 指定模块的路径
* --force-vermagic 忽略magic信息
* --force-modversion 忽略版本信息
* -f 强制
* -i 安装
* -n 测试模式
* -q 静默模式
* -R 跟踪alias
* -r 删除
* --show-depends 查看模块依赖

示例
^^^^

::

    modprobe -r thinkpad_acpi
