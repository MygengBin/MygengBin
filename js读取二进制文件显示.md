# js读取二进制文件显示

## 1.base64展示

```javascript
function arrayBufferToBase64(buffer) {
    var binary = ''
    var bytes = new Uint8Array(buffer)
    var len = bytes.byteLength
    for (var i = 0; i < len; i++) {
        binary += String.fromCharCode(bytes[i])
    }
    return window.btoa(binary)
}
//如果展示转成base64前面拼上data:image/jpeg;base64,
```

