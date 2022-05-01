# MySQL 8.0 创建node.js支持的用户

由于8.0更新的官方加密方式，所以导致了不支持。

```javascript
{
    "code":"ER_NOT_SUPPORTED_AUTH_MODE",
    "errno":1251,"sqlMessage":"Client does not support authentication protocol requested by server; consider upgrading MySQL client",
    "sqlState":"08004",
    "fatal":true
}
```

## 解决方案

### 1. 创建用户

```mysql
create user '#userName'@'#host' identified by '#passWord';
```

> **#userName** 代表你要创建的此数据库的新用户账号
> **#host** 代表访问权限，如下
>
> - %代表通配所有host地址权限(可远程访问)
> - localhost为本地权限(不可远程访问)
> - 指定特殊Ip访问权限 如10.138.106.102
>
> **#passWord** 代表你要创建的此数据库的新用密码

### 2. 重置密码和修改加密方式

```sql
alter user 'root'@'localhost' identified with mysql_native_password '123456';
```

