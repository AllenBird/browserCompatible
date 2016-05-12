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
 可以自己实现注册一个，如果有jquery的话，可以使用jquery的$.trim() 方法；
 也可以用过es5-shim,es5-sham解决
```

## for 循环正确使用
```
 var aArray = ["1", "2", "3", "4"];
 var oObject = {'name': 'Allen', 'age': '18'};
 
 for (var i in oObject){}
 for (var i; i < aArray.length; i++){}
```

## IE8 不支持 background-size
```
  补救方法如下： 
  background-image: url(/assets/images/*.png);
  background-image: none \9;
  background-size: cover;
  filter: progid:DXImageTransform.Microsoft.AlphaImageLoader(src='/assets/images/*.png',sizingMethod='scale');
```

## IE8 不支持4095以上各css对象
```
  这这这，只能优化代码了，还可以分域名，class样式省着用。
```

## IE8 float bug
```
  Actually, there is a bug in IE8 where right-floated elements seem to clear:left.
  http://blogs.msdn.com/b/askie/archive/2009/03/23/right-floated-element-in-internet-explorer-8-is-positioned-differently-than-internet-explorer-7.aspx

  If you don't want to add anything to your HTML at all, you can slightly restructure it for a quick fix. Put the right-floated sidebar first, ie:

  <div id="content-area" class="espacio">
    <div class="eltitular">HEADER</div>
    <div id="sidebar">RIGHT CONTENT</div>
    <div class="lacarta">LEFT CONTENT</div>
  </div>
```

## IE8 jquery css() bug
```
 NOT USED!
```
