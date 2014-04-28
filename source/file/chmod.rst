chmod
=====================================

简介
^^^^
改变文件或者目录的权限

选项
^^^^

* -R 递归式处理
* [ugoa][+-=][rwxXst] || [1234567]{3}

    * X execute/search only if the file is a directory or already has execute permission for some user 
    * s 授予文件以文件所有者/组的权限
    * t 限制删除和粘滞特性

示例
^^^^

改变文件属性::

    chmod u+w /path/to/file
