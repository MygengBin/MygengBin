# Express初始化

## 一、安装express库和生成器

```shell
npm i -g express express-generator

express --version #查看版本
```

>  上面里两个模块分别表示库和生成器，在express3时，安装express会自动的给你安装生成器express-generator ，但是在express4时，他们就被分开了，所以需要分别安装。

## 二、express生成器自动创建express项目

```sh
express nodejs #第二参数是项目文件名
#成功之后就可以进去了，然后安装依赖
```

## 三、安装依赖

```sh
npm i 
```

## 四、启动项目

```sh
npm run start 
# 打开浏览器，访问127.0.0.1:3000就能获取访问我们的项目了
```

## 五、项目目录解释

> bin：存放可执行文件
>
> public：存放js、css、img等文件
>
> router：存放路由文件
>
> views：存放视图文件或者说模版文件
>
> app.js：启动文件（入口文件）
>
> package.json：存储着工程的信息及模块依赖，当在 dependencies 中添加依赖的模块时，运行 npm install，npm 会检查当前目录下的 package.json，并自动安装所有指定的模块
>
> node_modules：存放 package.json 中安装的模块，当你在 package.json 添加依赖的模块并安装后，存放在这个文件夹下

## 六、在此项目中如何开发

首先在routes中新建一个test.js文件

```js
var express = require('express');
var router = express.Router();

router.get('/', function (req, res, next) {
	res.send('我是接口返回值');
});

module.exports = router;
```

然后在app.js中加入下面代码

```js
var testRouter = require('./routes/test');
app.use('/test', testRouter);
```



## 七、使用nodemon自动重启服务

### 1.安装nodemon

```sh
npm i nodemon -S
```

### 2.创建nodemon配置文件

```javascript
/*在项目的根目录下创建：nodemon.json文件*/
{
	"restartable": "rs",
	"ignore": [".git", ".svn", "node_modules/**/node_modules"],
	"verbose": true,
	"execMap": {
		"js": "node --harmony"
	},
	"watch": [],
	"env": {
		"NODE_ENV": "development"
	},
	"ext": "js json njk css js "
}
```

### 3.package.json配置

```json
/*在scripts里面添加，第二个参数为要启动的目录或文件，默认index可以省略不写*/
dev:"nodemon ./bin/www"
```

