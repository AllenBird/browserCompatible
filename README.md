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
