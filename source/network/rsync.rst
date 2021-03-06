rsync
=====================================

简介
^^^^
高效文件拷贝工具

选项
^^^^

* -v, --verbose 增强可读性
* -q, --quiet 忽略非错误信息
* --no-motd 忽略daemon模式的MOTD信息 (see manpage caveat)
* -c, --checksum 基于checksum校验，而非mod-time和size
* -a, --archive 归档模式，和-rlptgoD (不要使用 -H,-A,-X)参数相同
* --no-OPTION 关闭一些显式的OPTION (比如 --no-D)
* -r, --recursive 递归目录
* -R, --relative 使用相对路径
* --no-implied-dirs 不发送制定目录的属性，避免在目标使用--relative删除连接重新传输文件
* -b, --backup 备份 (查看 --suffix & --backup-dir)
* --backup-dir=DIR 基于DIR来创建备份的目录结构
* --suffix=SUFFIX 制定备份的后最 (default ~ w/o --backup-dir)
* -u, --update 跳过接受端较新的文件
* --inplace 直接在文件上更新(SEE MAN PAGE)
* --append 直接追加文件
* --append-verify 和--append很像, 只是用文件的较旧的那部份做checksum
* -d, --dirs 仅传输文件而非递归
* -l, --links 将软链接当作软链接来拷贝
* -L, --copy-links 拷贝链接对应的文件或者目录而非链接本身
* --copy-unsafe-links 仅不安全的链接才被拷贝
* --safe-links 忽略那些链接到目录树外的链接
* -k, --copy-dirlinks 将链接翻译成其链接的目录
* -K, --keep-dirlinks 将目录链接在接收端转换成目录
* -H, --hard-links 保留硬链接
* -p, --perms 保留权限
* -E, --executability 保留文件的可执行性
* --chmod=CHMOD 改变文件或者目录的权限
* -A, --acls 保留ACLs (implies --perms)
* -X, --xattrs 保留扩展属性
* -o, --owner 保留所有者(super-user only)
* -g, --group 保留组
* --devices 保留设备文件 (super-user only)
* --specials 保留特殊文件
* -D 和 --devices --specials一样
* -t, --times 保留修改时间
* -O, --omit-dir-times 在--times选项里忽略目录的时间
* --super 允许接受方执行那个一些超级用户的活动
* --fake-super 通过xattrs来存储和回复权限
* -S, --sparse 高效处理稀疏文件
* -n, --dry-run 只运行，不做改变
* -W, --whole-file 拷贝整个文件(without delta-xfer algorithm)
* -x, --one-file-system 不跨越文件系统
* -B, --block-size=SIZE 强制指定checksum的块大小
* -e, --rsh=COMMAND 指定要使用的远程shell
* --rsync-path=PROGRAM 指定远程要运行的rsync路径
* --existing 如果接收端不存在文件就不创建
* --ignore-existing 如果接收端存在就不更新文件
* --remove-source-files 发送端删除已经同步的文件 (non-dirs)
* --del an alias for --delete-during
* --delete 删除接收端上在发送端不存在的文件
* --delete-before 接收端在发送前删除，而不是发送过程中
* --delete-during 接收端在发送过程中删除
* --delete-delay 在发送过程中寻找文件，在发送完成后删除
* --delete-after 接收端在发送完成后删除
* --delete-excluded 在接收端删除排除的文件
* --ignore-errors 即使有I/O错误也删除
* --force 即使目录不是空的也删除
* --max-delete=NUM 最多删除文件的数目
* --max-size=SIZE 最大传输文件的大小
* --min-size=SIZE 最小传输文件的大小
* --partial 保持部分传输的文件
* --partial-dir=DIR 制定部分传输文件的存放目录
* --delay-updates 先传输，最后再更新，保持原子性
* -m, --prune-empty-dirs 接收端删除空目录
* --numeric-ids 接收端不要将uid/gid映射为用户名和组名
* --timeout=SECONDS 设置I/O超时时间，s为单位
* --contimeout=SECONDS 设置链接服务端的时间
* -I, --ignore-times 即使mtime和size都相同也不跳过
* --size-only 只要大小相同就跳过
* --modify-window=NUM 比对时间时制定精确范围，范围内都认为时间相同
* -T, --temp-dir=DIR 指定创建临时文件的目录
* -y, --fuzzy 文件在接收端不存在的情况下，在当前目录下寻找一个基础文件，以加快传输
* --compare-dest=DIR 接收端除了和发送端对比还和这里指定的目录对比，适合备份上次备份改变的文件
* --copy-dest=DIR 和--compare-dest类似，只是接收端会用本地拷贝来复制那些未改变的文件
* --link-dest=DIR 和--compare-dest类似，只是接收端会建立那些未改变文件的硬链接
* -z, --compress 传输过程中压缩
* --compress-level=NUM 指定压缩等级
* --skip-compress=LIST 不压缩指定后缀的文件
* -C, --cvs-exclude 以CSV的方式自动忽略文件
* -f, --filter=RULE 新增一个file-filtering规则
* -F same as --filter='dir-merge /.rsync-filter' repeated: --filter='- .rsync-filter'
* --exclude=PATTERN 排除规则PATTERN
* --exclude-from=FILE 从文件中读取排除规则
* --include=PATTERN 不要排除指定规则的文件
* --include-from=FILE 从文件中读取包含的规则
* --files-from=FILE 从文件中读取文件列表
* -0, --from0 all 
* -from/filter files are delimited by 0s
* -s, --protect-args 参数不许要空格分割; only wildcard special-chars
* --address=ADDRESS 绑定监听的地址
* --port=PORT 制定端口号
* --sockopts=OPTIONS 制定TCP选项
* --blocking-io 在远程shell中使用blocking I/O
* --stats 给出文件统计信息
* -8, --8-bit-output 输出时不对高位字符转义
* -h, --human-readable 以易于阅读的方式打印数字
* --progress 显示传输进度
* -P same as --partial --progress
* -i, --itemize-changes 打印更新的总结信息
* --out-format=FORMAT 以特定的格式打印更新信息
* --log-file=FILE 日志文件
* --log-file-format=FMT 日志文件格式
* --password-file=FILE 密码文件
* --list-only 仅列出文件
* --bwlimit=KBPS 限制带宽; KBytes per second
* --write-batch=FILE 将批量更新写入文件
* --only-write-batch=FILE 和 --write-batch类似 but w/o updating destination
* --read-batch=FILE 从文件中读取批量更新任务
* --protocol=NUM 使用旧版本的协议
* --iconv=CONVERT_SPEC 要求文件名字符转义
* -4, --ipv4 prefer IPv4
* -6, --ipv6 prefer IPv6
* --version 打印帮助信息
* (-h) --help 打印这个帮组信息 (-h 仅在单独使用时与 --help 同意)

示例
^^^^

镜像::

    rsync -az -e ssh --delete /local/ remote:/remote/

快速删除::

    mkdir /tmp/blank/ && rsync -av --delete /tmp/blank/ /dest/path/
