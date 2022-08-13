# Centos8安装docker

yum install docker-ce

# docker安装mysql

```sh
docker run -p 3306:3306 --name mysql8.0 -e MYSQL_ROOT_PASSWORD=1234 -d mysql
```

> run启动
>
> -p的参数第一个是操作系统的，第二个是docker镜像的
>
> -name是启动的这个容器的名字
>
> -e MYSQL_ROOT_PASSWORD 是设置mysql初始密码
>
> -d mysql是镜像名称，没有规定版本默认是最新的，如果规定可以mysql:8.0.29

```sh
docker ps -a #查看启动的容易
docker images #查看本地的镜像
docker exec -it mysql8.0 bash #进入这个名字的docker容器
mysql -uroot -p #连接mysql 回车后输入密码，输入密码不提示
```

```mysql
alter user 'root'@'%' identified with mysql_native_password by '1234';#设置远程连接和重置密码
select host,user,plugin,authentication_string from mysql.user; #查看设置是否成功
```

每一个docker容器是独立运行的，在建立mysql第二个docker的端口仍然可以用3306，但是name不能相同

# docker进入容器报：Error response from daemon: Container ******* is not running

原因是docker容器未启动，已经存在

```sh
docker ps -a #查看所有的容器
docker rm containerId # 删除容器
docker start containerId # 启动容器
```

