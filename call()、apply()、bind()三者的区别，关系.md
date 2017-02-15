#### call()、apply() 都是函数方法,都可以扩充函数作用域

调用这两个函数，都可以改变函数this指向

```
function saycolor () {
  alert (this.color);
}
var o = {color : "red"};
var o1 = {color : "blue"}
saycolor.call(o);//red
saycolor.apply(o1);//blue
```



#### call()、apply() 作用相同，传入的参数形式不同

call() 除了第一个参数，其余的参数直接传入，须逐个列举出来；而apply() 第二个参数以数组的形式传入

```
function sum (arg1, arg2) {
  return arg1 + arg2;
}
function sum1 (arg1, arg2) {
  return sum.call(this,arg1,arg2);
}
function sum2 (arg1, arg2) {
  return sum.apply(this,arguments);
}
sum1(2,3);//5
sum2(1,5);//6
```

在某个函数的参数个数不确定的时候用apply，在函数的参数个数确定时用call

#### bind() 创建一个函数的实例

bind() 方法会创建一个新函数，称为绑定函数，当调用这个函数时，绑定函数会以创建它时传入bind() 方法时的第一个参数作为this，传入bind() 方法的第二个以及以后的参数加上绑定函数运行时本身的参数按照顺序作为原函数的参数来调用原函数。bind() 也可以改变函数的this指向。

```
window.color = "red";
var o = {color: "blue"};
function sayColor () {
  alert (this.color);
}
var objSayColor = sayColor.bind(o);
objSayColor();
```

bind() 不会立即执行，是在回调执行的时候调用bind()方法



#### 总结

* apply、call、bind 都可以改变函数this指向，其中第一个参数都是this要指向的对象，也就是指定上下文；
* apply、call、bind三者都可以利用后续参数传参
* bind 是返回对应函数，便于稍后调用；apply、call则是立即调用