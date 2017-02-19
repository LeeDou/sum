1. 选取DOM元素
 > $(".class") 等选择功能，在控制台可以直接使用
 > $$('tagName')或$$('.class')可以将选择的dom节点放进一个数组中

1. 将浏览器变成编辑器

在控制台输入`document.body.contentEditable= true;`

1. 查找DOM中元素关联的事件
> `getEventListeners($('selector')).eventName[0].listener`

4.查询代码执行时间
```
console.time("mytime");
console.timeEnd("mytime");
```

5.将变量里的表格排列成表格
比如有一个对象数组：

```
var myArray = [{a:1,b:2},{a:4,b:5},{k:6,d:10}];
console.log.table(myarry);
```


6.检查DOM中的元素
可以直接在制检查元素
* inspect($('selector')) 会检查与选择器匹配的元素，并且换到开发者元素标签页
* $0 、$1、$2 能帮你取到最近选择的元素
  7.列举元素的属性
  dir($('sector')) 可以在控制台中列举一个元素的所有属性

8.检索最近一个元素的值
$_ 
9.清空控制台和内存
> clear()

