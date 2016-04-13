# 前端浏览器兼容
政采云遇到的兼容性问题汇总
## ECMAScript 6 的方法不能直接用。
```
IE11 & Chrome 是支持Map() Set() 的，但是firefox和safari不支持。
new Map(), Set();
```

## IE下，标签 ` li ` 的属性 ` value ` 的特技

* ` value="" `  
	 => ` value="1" `
* ` value="02" `  
	 => ` value="2" `

## IE8下的localstorage 的清除不支持 delete方法
```
 理论上localstorage也应该正规用removeItem这个方法吧。
```

## IE8下的string 不支持 trim方法
```
 可以自己实现注册一个，如果有jquery的话，可以使用jquery的$.trim() 方法
```
