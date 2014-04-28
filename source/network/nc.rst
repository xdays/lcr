nc
=====================================

简介
^^^^
创建TCP或者UDP连接和监听

选项
^^^^

* -C 发送CRLF换行符
* -D 开启debug
* -I TCP接收buffer
* -i 接收时间间隔
* -k 完成连接后不断开连接
* -l 监听模式
* -n 不做域名解析
* -O TCP发送buffer
* -p 端口
* -r 端口随机选择
* -s 源IP
* -u 使用UDP协议
* -w 超时时间
* -z 扫描端口

示例
^^^^

传文件::

    接收：
    nc -l 8888 > /path/file
    发送：
    nc 127.0.0.1 88888 > /path/file

远程执行命令::

    服务端：
    rm -f /tmp/f; mkfifo /tmp/f
    cat /tmp/f | /bin/sh -i 2>&1 | nc -l 127.0.0.1 1234 > /tmp/f
    客户端：
    nc 127.0.0.1 1234

端口扫描::

    nc -zv host.example.com 20-30
