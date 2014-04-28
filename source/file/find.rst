find
=====================================

简介
^^^^
按一定条件查找文件，对找到的文件做一些操作。

选项
^^^^

* -H 不跟踪链接，除非用链接作为参数
* -L 跟踪链接
* -P 从不跟踪链接
* -D debug模式
* -O 优化等级0123
* 表达式，包括选项，探测规则和执行的操作组成，由操作符链接，默认是-and，其他有-or

    * 选项

        * -d/-depth 先查找目录下的东东，再查找目录
        * -daystart 时间从今天的开始算起而不是24小时前
        * -maxdepth 最大深度
        * -mindepth 最小深度
        * -regextype 正则的类型emacs(default), posix-awk, posix-basic, posix-egrep 和 posix-extended
        * -mount/-xdev 不查找其他文件系统下的文件

    * 探测规则

        * +n/-n/n 大于/小于/等于n
        * -amin/-cmim/-mmin 以分钟算检测atime/ctime/mtime
        * -anewer/-cnewer atime/ctime晚于mtime
        * -atime/-ctime/-mtime 默认是h
        * -empty 空文件
        * -executable 可执行
        * -false 就是false
        * -fstype 文件所在的文件系统
        * -gid/-group 组
        * -iname
        * -inum inode号
        * -links 连接数
        * -lname/-ilname 链接的目标
        * -name/-iname 文件名
        * -newer file mtime比file新
        * -newerXY reference 和参考文件多重比较
        * -nogroup/-nouser 没有组/用户和此ID对应
        * -path 路径
        * -perm 权限
        * -readable 通过access命令可读
        * -regex/-iregex 正则匹配
        * -samefile file 和file有相同的inode
        * -size 文件大小
        * -true 就是true
        * -uid/-user 用户
        * -used 文件改变n天后被访问
        * -wholename/-iwholename 路径
        * -writable 通过access可写
        * -xtype 和-type一样，只是针对链接

    * 操作

        * -delete 删除
        * -exec command {} \; 执行命令，类似xargs
        * -fls file 类似ls，只是将结果写入文件
        * -fprint/-fprintf file 同上，写文件绝对路径/以prindf格式写
        * -ls 以ls -dils格式显示文件

示例
^^^^

查找当前目录::

    find . -mtime +5min -type f -size 1M -exec rm -f {} \;
