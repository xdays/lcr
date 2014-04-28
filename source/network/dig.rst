dig
=====================================

简介
^^^^
域名解析工具

选项
^^^^

* -b 绑定地址
* -f 批量执行，从文件读取
* -m 开启内存调试
* -p 端口
* -4 ipv4
* -t 查询类型
* -q 查询域名
* -k/-y 带签名发送请求
* 查询选项

    * +[no]tcp 使用tcp
    * +[no]vc 使用tcp
    * +[no]ignore 忽略UDP分片
    * +domain 指定域
    * +[no]search 使用resolv.conf的search配置
    * +[no]aaonly/aaflag 请求是添加aa标志
    * +[no]adonly 请求是添加ad标志
    * +[no]cdonly 请求是添加cd标志
    * +[no]cl 输出class
    * +[no]ttlid 输出ttl
    * +[no]recurse 递归查询
    * +[no]nssearch 获取授权服务器信息
    * +[no]trace 追踪
    * +[no]cmd 输出详细信息
    * +[no]short 简单的输出
    * +[no]identify 现实服务器信息
    * +[no]comments 输出注释信息
    * +[no]rrcomments 每个请求输出
    * +split=w 分割
    * +[no]stats 统计信息
    * +[no]qr 不输出请求信息
    * +[no]question 请求信息
    * +[no]answer 响应信息
    * +[no]authority 授权信息
    * +[no]additional 额外信息
    * +[no]all 设置或者清空所有的flag
    * +time=t 超时时间
    * +tries=t 请求次数
    * +retries=t 重新请求次数
    * +ndots=t 域名中出现几个点认为是绝对域名
    * +bufsize=b 缓存大小
    * +edns=# EDNS版本
    * +[no]multiline 增强可读性
    * +[no]onesoa 只打印一个授权
    * +[no]fail 如果遇到SERVFAIL错误就不继续尝试
    * +[no]besteffort 输出mailform的信息
    * +[no]dnssec 发送DNSSEC请求
    * +[no]sigchase 签名
    * +trusted-ky=### 签名文件
    * +[no]topdown 执行top-down检查
    * +[no]nsid 请求是包含EDNS的服务器ID信息

示例
^^^^

::

    dig @8.8.8.8 www.xdays.info +short
