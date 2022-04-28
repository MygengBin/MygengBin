# 隐藏electron窗体菜单栏的几种方式

方法1：

```javascript
const electron = require('electron')
const Menu = electron.Menu
function createWindow (){
	Menu.setApplicationMenu(null)
}
```

方法2：

```javascript
new BrowserWindow（{autoHideMenuBar： true}）
```

方法3：

```javascript
new BrowserWindow（{frame: false}）
```

