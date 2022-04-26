# JS判断当前语言
国际化的英文单词是Internationalization，因为这个单词太长了，所以有时简称I18N，其中18是I和N之间省略的18个字母。

此功能通过navigator完成

它的两个属性和语言相关分别是`language`和`languages`

通常使用language代表用户偏向语言，大概率自己设置的

## 保存语言选项

一般可以把语言存到本地缓存或者Cookie

```javascript
//获取cookie中的默认语言
export const getCookieLang = function() {
  let strcookie = document.cookie; //获取cookie字符串
  let arrcookie = strcookie.split(";"); //分割
  let cookieLang = "";
  for (let i = 0; i < arrcookie.length; i++) {
    let arr = arrcookie[i].split("=");
    //当cookie语言相关的键名为：org.springframework.web.servlet.i18n.CookieLocaleResolver.LOCALE
    if (
      arr &&
      arr[0].trim() ==
        "org.springframework.web.servlet.i18n.CookieLocaleResolver.LOCALE"
    ) {
      cookieLang = arr[1];
      break;
    }
  }
  return cookieLang;
};
```

```javascript
// 获取浏览器默认语言
export const getBrowserLang = function() {
  let browserLang = navigator.language
    ? navigator.language
    : navigator.browserLanguage;
  let defaultBrowserLang = "";
  if (
    browserLang.toLowerCase() === "us" ||
    browserLang.toLowerCase() === "en" ||
    browserLang.toLowerCase() === "en_us"
  ) {
    defaultBrowserLang = "en_US";
  } else {
    defaultBrowserLang = "zh_CN";
  }
  return defaultBrowserLang;
};
```

此时，当前系统语言 通过 cookie存储的语言和浏览器语言同时判断：

```javascript
// 获取当前系统语言（首先从cookie里获取，默认为浏览器当前的语言）
let cookieLang = getCookieLang();
cookieLang = cookieLang === "en" || cookieLang === "us" ? "en_US" : cookieLang;
const lang = cookieLang || getBrowserLang();
console.log(lang)        //这里的lang代表当前项目使用的语言
```