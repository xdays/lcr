wget
=====================================

简介
^^^^
非交互式下载器

选项
^^^^

Startup::

    -V,  --version           display the version of Wget and exit. 查看版本信息
    -h,  --help              print this help. 打印这个帮助文档
    -b,  --background        go to background after startup. 启动后放到后台
    -e,  --execute=COMMAND   execute a `.wgetrc'-style command. 执行wgetrc格式的命令

Logging and input file::

    -o,  --output-file=FILE    log messages to FILE. 日志输出到文件
    -a,  --append-output=FILE  append messages to FILE. 日志附加到文件
    -d,  --debug               print lots of debugging information. 启动debug模式
    -q,  --quiet               quiet (no output). 静默执行
    -v,  --verbose             be verbose (this is the default). 输出长信息
    -nv, --no-verbose          turn off verboseness, without being quiet. 关闭长信息，非静默执行
    -i,  --input-file=FILE     download URLs found in FILE. 下载文件中包含的URL
    -F,  --force-html          treat input file as HTML. 把输入文件当成HTML对待
    -B,  --base=URL            prepends URL to relative links in -F -i file. 在输入文件的路径前加相对URL

Download::

    -t,  --tries=NUMBER            set number of retries to NUMBER (0 unlimits). 尝试次数
         --retry-connrefused       retry even if connection is refused. 执着模式，即使被拒绝了也加班
    -O,  --output-document=FILE    write documents to FILE. 将下载的文档写入文件
    -nc, --no-clobber              skip downloads that would download to 
                                   existing files. 如果下载的文件已存在就跳过下载
    -c,  --continue                resume getting a partially-downloaded file. 断点续传功能
         --progress=TYPE           select progress gauge type. 选择进度记录类型
    -N,  --timestamping            don't re-retrieve files unless newer than
                                   local. 除非文件比现有的新，否则不下载
    -S,  --server-response         print server response. 打印服务器响应
         --spider                  don't download anything. 不下载任何东西，就是爬一下
    -T,  --timeout=SECONDS         set all timeout values to SECONDS. 设置所有的超时时间
         --dns-timeout=SECS        set the DNS lookup timeout to SECS. 设置DNS的超时时间
         --connect-timeout=SECS    set the connect timeout to SECS. 设置连接的超时时间
         --read-timeout=SECS       set the read timeout to SECS. 设置读取的超时时间
    -w,  --wait=SECONDS            wait SECONDS between retrievals. 两次获取之间的等待时间
         --waitretry=SECONDS       wait 1..SECONDS between retries of a retrieval.  在重新获取之间等待时间
         --random-wait             wait from 0...2*WAIT secs between retrievals. 获取之间等待时间，晕了~
         --no-proxy                explicitly turn off proxy. 关闭代理
    -Q,  --quota=NUMBER            set retrieval quota to NUMBER. 设置获取配额
         --bind-address=ADDRESS    bind to ADDRESS (hostname or IP) on local host. 绑定本地特定的地址
         --limit-rate=RATE         limit download rate to RATE. 下载限速
         --no-dns-cache            disable caching DNS lookups. 关闭DNS解析
         --restrict-file-names=OS  restrict chars in file names to ones OS allows. 限制文件名中出现的字符
         --ignore-case             ignore case when matching files/directories. 匹配文件或目录时忽略大小写
    -4,  --inet4-only              connect only to IPv4 addresses. 仅连接ipv4地址
    -6,  --inet6-only              connect only to IPv6 addresses. 仅连接ipv6地址
         --prefer-family=FAMILY    connect first to addresses of specified family,
                                   one of IPv6, IPv4, or none. 首先连接指定的地址类型
         --user=USER               set both ftp and http user to USER. 设置http或者ftp的用户名
         --password=PASS           set both ftp and http password to PASS. 设置http或者ftp的密码

Directories::

    -nd, --no-directories           don't create directories. 不创建目录
    -x,  --force-directories        force creation of directories. 强制创建
    -nH, --no-host-directories      don't create host directories. 创建本机目录
         --protocol-directories     use protocol name in directories. 在目录名中用协议名
    -P,  --directory-prefix=PREFIX  save files to PREFIX/... 将文件保存到特定目录下
         --cut-dirs=NUMBER          ignore NUMBER remote directory components. 没看懂~

HTTP options::

    --http-user=USER        set http user to USER. 设置http用户
    --http-password=PASS    set http password to PASS. 设置http密码
    --no-cache              disallow server-cached data. 告诉server不要缓存的内容
    -E,  --html-extension        save HTML documents with `.html' extension. 以html后缀保存文件
         --ignore-length         ignore `Content-Length' header field. 忽略内容长度报头header
         --header=STRING         insert STRING among the headers. 插入header字段
         --max-redirect          maximum redirections allowed per page. 每个网页最大跳转数
         --proxy-user=USER       set USER as proxy username. 设置代理用户
         --proxy-password=PASS   set PASS as proxy password. 设置代理密码
         --referer=URL           include `Referer: URL' header in HTTP request. 请求中包含referer这个header
         --save-headers          save the HTTP headers to file. 把header保存到文件中
    -U,  --user-agent=AGENT      identify as AGENT instead of Wget/VERSION. 指定agent
         --no-http-keep-alive    disable HTTP keep-alive (persistent connections). 关闭keep-alive
         --no-cookies            don't use cookies. 不适用cookie
         --load-cookies=FILE     load cookies from FILE before session. 在会话之前从文件中载入cookie
         --save-cookies=FILE     save cookies to FILE after session. 将cookie保存到文件中
         --keep-session-cookies  load and save session (non-permanent) cookies. 保存并载入cookie
         --post-data=STRING      use the POST method; send STRING as the data. 用post方法时发送的字符
         --post-file=FILE        use the POST method; send contents of FILE. 用post方法，发送文件内容
         --content-disposition   honor the Content-Disposition header when 
                                 choosing local file names (EXPERIMENTAL). 没看懂~
         --auth-no-challenge     Send Basic HTTP authentication information
                                 without first waiting for the server's
                                 challenge. 不等待server端发起challenge请求直接发送基本的验证信息

HTTPS (SSL/TLS) options::

         --secure-protocol=PR     choose secure protocol, one of auto, SSLv2,
                                  SSLv3, and TLSv1.选择安全协议类型
         --no-check-certificate   don't validate the server's certificate. 不验证服务器证书
         --certificate=FILE       client certificate file. 客户端证书文件
         --certificate-type=TYPE  client certificate type, PEM or DER. 客户端证书类型
         --private-key=FILE       private key file. 私钥文件
         --private-key-type=TYPE  private key type, PEM or DER. 私钥类型
         --ca-certificate=FILE    file with the bundle of CA's. 没看懂~
         --ca-directory=DIR       directory where hash list of CA's is stored. 没看懂~
         --random-file=FILE       file with random data for seeding the SSL PRNG. 没看懂~
         --egd-file=FILE          file naming the EGD socket with random data. 没看懂~

FTP options::

         --ftp-user=USER         set ftp user to USER. 设置ftp用户
         --ftp-password=PASS     set ftp password to PASS. 设置ftp密码
         --no-remove-listing     don't remove `.listing' files. 不删除.listing文件
         --no-glob               turn off FTP file name globbing. 关闭ftp文件名替换
         --no-passive-ftp        disable the "passive" transfer mode. 关闭被动模式
         --retr-symlinks         when recursing, get linked-to files (not dir). 没看懂~
         --preserve-permissions  preserve remote file permissions. 保留服务器端文件权限

Recursive download::

    -r,  --recursive          specify recursive download. 指定递归下载
    -l,  --level=NUMBER       maximum recursion depth (inf or 0 for infinite). 最大递归深度
         --delete-after       delete files locally after downloading them. 下载完成后本地删除文件
    -k,  --convert-links      make links in downloaded HTML point to local files. 没看懂~
    -K,  --backup-converted   before converting file X, back up as X.orig. 转换前备份文件
    -m,  --mirror             shortcut for -N -r -l inf --no-remove-listing. 镜像站点用的吧
    -p,  --page-requisites    get all images, etc. needed to display HTML page. 下载所有网页上呈现的所有元素
         --strict-comments    turn on strict (SGML) handling of HTML comments. 开启严格处理HTML注释

Recursive accept/reject::

    -A,  --accept=LIST               comma-separated list of accepted extensions. 逗号分隔的可以接受的拓展名
    -R,  --reject=LIST               comma-separated list of rejected extensions. 逗号分隔的拒绝接受的扩展名
    -D,  --domains=LIST              comma-separated list of accepted domains. 逗号分隔的可以接受的域名
         --exclude-domains=LIST      comma-separated list of rejected domains. 逗号分隔的决绝接受的域名
         --follow-ftp                follow FTP links from HTML documents. 接受从HTML到ftp的跳转
         --follow-tags=LIST          comma-separated list of followed HTML tags. 逗号分隔的可接受的跳转HTML标签
         --ignore-tags=LIST          comma-separated list of ignored HTML tags. 逗号分隔的拒绝接受的HTML标签
    -H,  --span-hosts                go to foreign hosts when recursive. 当递归的时候可以到外面的host
    -L,  --relative                  follow relative links only. 仅仅跳转相对链接
    -I,  --include-directories=LIST  list of allowed directories. 允许的目录列表
    -X,  --exclude-directories=LIST  list of excluded directories. 排除的目录列表
    -np, --no-parent                 don't ascend to the parent directory. 不追溯父目录

示例
^^^^

镜像站点::

    wget -c -r -np -k -L -b --reject=gif http://mirrors.163.com/centos/6/os/x86_64/ -e robots=off
