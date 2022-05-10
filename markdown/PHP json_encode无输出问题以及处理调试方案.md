# PHP json_encode无输出问题以及处理调试方案

问题原因：在select *的时候有一个blob存二进制的字段。导致的结果是发现一直输出空白，但如果使用`print_r()`就又有输出，怀疑是`json_encode()`函数有问题。

## 问题思路

1. 首先尝试了直接输出`$res` 发现没问题，显示Array说明有数值
2. 然后直接`echo json_encode(某数组)`，发现也没有输出，那必定是这个函数的问题

## 解决思路

首先查网上资料，发现`json_encode()`函数也有调试模式`json_last_error()`，只要在输出后加上`var_dump(json_last_error());`就能知道函数哪里出问题了

```php
echo json_encode(array('error' => '0', 'message' => '没有错误'));
var_dump(json_last_error());
//这里也可以是json_decode

//错误码对照
0 JSON_ERROR_NONE
1 JSON_ERROR_DEPTH
2 JSON_ERROR_STATE_MISMATCH
3 JSON_ERROR_CTRL_CHAR
4 JSON_ERROR_SYNTAX
5 JSON_ERROR_UTF8
6 JSON_ERROR_RECURSION
7 JSON_ERROR_INF_OR_NAN
8 JSON_ERROR_UNSUPPORTED_TYPE
    
// 我记得当时报的信息是这个 Malformed UTF-8 characters, possibly incorrectly encoded
```

如果返回5，那么就要把gb2312编码部分的中文转换成UTF8输出

那么用`iconv('gbk', 'utf-8', $data)`函数就解决了
