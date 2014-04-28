tar
=====================================

简介
^^^^

归档工具，和cpio类似


选项
^^^^

* -c 创建归档
* -f 指定归档文件
* -j 调用bzip2压缩或者解压归档
* -l 查看归档内容
* -x 解压归档
* -z 调用gzip压缩或者解压归档

示例
^^^^

打包压缩文件::

    tar -czf foobar.tar.gz foo bar

解压文件::

    tar -xzf foobar.tar
