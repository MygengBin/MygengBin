# PHP上传文件失败总结

## 1.查找原因 

```php
var_dump($_FILES['FileName']);
```

### 其中error返回的错误代码

```php
// 0 UPLOAD_ERR_OK 上传成功
// 1 UPLOAD_ERR_INI_SIZE 上传的文件超过了php.ini中upload_max_filesize选项限制的值
// 2 UPLOAD_ERR_FROM_SIZE 上传文件超过了HTML中MAX_FILE_SIZE的大小
// 3 UPLOAD_ERR_PARTIAL 文件只有部分被上传
// 4没用文件被上传
// 5上传文件大小为0
```

### 其他配置

```php
// 1.file_uploads=on/off 是否允许通过http方式上传文件 
// 2.max_execution_time=30 允许脚本最大执行时间，超过这个时间就会报错 
// 3.memory_limit=50M 设置脚本可以分配的最大内存量，防止失控脚本占用过多内存，此指令只有在编译时设置了 –enable-memory-limit标志的情况下才生效 
// 4.upload_max_filesize=20M 允许上传文件的最大大小，此指令必须小于post_max_size 
// 5.upload_tmp_dir 上传文件临时存放目录 
// 6.post_max_size=30M 允许post方式可以接受最大大小 
```

> 另外补充：文件上传结束后去向文件被上传结束后，默认地被存储在了临时目录中，这时您必须将它从临时目录中删除或移动到其它地方，如果没有，则会被删除。也就是不管是否上传成功，脚本执行完后临时目录里的文件肯定会被删除。

## 2. 原因2查找：

脚本停止运行附：修改PHP上传文件大小限制的方法

`在这里插入代码片`一般的文件上传,除非文件很小.就像一个5M的文件,很可能要超过一分钟才能上传完. 但在php中,默认的该页最久执行时间为 30 秒.就是说超过30秒,该脚本就停止执行.

这就导致出现 无法打开网页的情况.这时我们可以修改 max_execution_time在php.ini里查找`max_execution_time `默认是30秒.改为`max_execution_time = 0 `0表示没有限制

## 3. 原因3查找：

post_max_size修改 post_max_size 设定 POST 数据所允许的最大大小。此设定也影响到文件上传。

php默认的post_max_size 为2M.如果 POST 数据尺寸大于 post_max_size $_POST 和 $_FILES superglobals 便会为空. 

查找 post_max_size .改为`post_max_size = 150M `很多人都会改了第二步.

但上传文件时最大仍然为 8M. 为什么呢.我们还要改一个参数upload_max_filesize 表示所上传的文件的最大大小。

查找upload_max_filesize,默认为8M改为`upload_max_filesize = 100M `

另外要说明的是,post_max_size 大于 upload_max_filesize 为佳.

