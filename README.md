> 一个小而快的GBK库,支持浏览器

### 说明：
- 编码表是经过简单压缩的,最后打包出的min版只有不到30k(gzip 后20k)
	> 正常的编码表可能要到200K以上
- 本库不包含GBK自定义（扩展）码区
- 实现了URI相关函数,方便使用
- 浏览器请使用 `dist/` 路径下的文件
- 浏览器版本加载时会解压编码表,建议异步加载

## API

### GBK.encode({string}) 解码GBK为一个字节数组
```
GBK.encode('时顺地?abc地')
> [ 202, 177, 203, 179, 181, 216, 63, 97, 98, 99, 181, 216 ]
```

### GBK.decode({BbyteArry}) 解码GBK编码的字节数组 返回字符串
```
GBK.decode([ 202, 177, 203, 179, 181, 216, 63, 97, 98, 99, 181, 216 ])
> 时顺地?abc地;
```