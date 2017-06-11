# 原型模式

### 实现方式一: 通过Object.create()方式来实现

```
var myCar = {
	name: "kantle",

	drive: function () {
		console.log("I am driving!");
	},
	panic: function () {
		console.log("Wait, how do you stop this thing")
	},
};

// 使用Object.create实例化一个新car
var yourCar = Object.create(myCar);

// 现在可以看到一个对象是另一个对象的原型
console.log(yourCar.name)
```

### 方式二： 不直接使用Object.create()方式实现

```
var vehiclePrototype = {
	init: function (carModel) {
		this.model = carModel;
	},

	getModel: function () {
 		console.log("The model of this vehicle is.." + this.model);
	}
};

function vehicle (model) {
	function F() {};
	F.prototype = vehiclePrototype;
	var f = new F();
	f.init(model);
	return f;
}

var car = vehicle("kantle");
car.getModel();
```

### 实现方式三： 
```
var car = vehicle("kantle");
car.getModel();

var beget = (function(){

	function F() {};
	return function (proto) {
		F.prototype = proto;
		return new F()
	}
})();
```