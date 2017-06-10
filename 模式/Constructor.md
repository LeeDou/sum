## 构造器模式

### 基本的构造器模式
```
function car (year,miles){
  this.year = year;
  this.miles = miles;
  this.toString = function() {
    return this.miles + "has done" + this.year
  }
}

var c = new car(2009,20000);
var d = new car(2008,30000);
console.log(c.toString());
console.log(d.toString());
```

### 带原型的构造器模式
```
function car (year,miles){
  this.year = year;
  this.miles = miles;
}
car.prototype.toString = function() {
  return this.miles + "has done" + this.year
}


var c = new car(2009,20000);
var d = new car(2008,30000);
console.log(c.toString());
console.log(d.toString());
```