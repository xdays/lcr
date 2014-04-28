ls
=====================================

简介
^^^^
列举目录内容

选项
^^^^

* -a/A 列举所有内容/除了.和..
* -b 打印转移字符
* --block-size= 指定块大小
* -c 以ctime来排序
* -C 按栏打印
* -d 打印目录本身而不是目录内容
* -F 分类
* --format= 打印格式有across(-x),commas(-m),horizontal(-x),long(-l),single-column(-1),verbose(-l),vertical(-C)
* -g 打印所属组
* -G 不打印所属组
* -h 易读方式
* --si 使用1000进制
* -i 打印inode号
* -k 以k为单位
* -l 详细信息
* -m 以逗号分割
* -o 打印所有者
* -Q 以双引号包含文件
* -R 递归式列举目录
* -s 显示大小
* -S 以大小排序
* --sort= 按指定模式排序none(-U),extension(-X),size(-S),time(-t),version(-v)
* --time= 按指定时间排序atime(-u),access(-u),use(-u),ctime(-c),status(-c)
* --time-style= 时间显示格式full-iso,locale
* -x 以horizontal方式显示文件
* -1 以行显示文件

示例
^^^^

以mtime排序显示文件::

    ls -l --time=ctime $HOME
