# 单例模式

### 限制了实例化的次数只能一次。

### 单例模式的实现
```
var mySingleton = (function (){
	// 实例保持了Singleton的一个引用
	var instance;
	function init() {
		// singleton
		// 私有方法和变量
		function privateMethod() {
			console.log("i am private");
		}
		var privateVariable = "Im also private";
		var privateRandomNumber = Math.random();
		return {
			publicMethod: function () {
				console.log("The public can see me!");
			},
			publicProperty: "I am also public",
			getRandomNumber: function () {
				return privateRandomNumber;
			}

		}
	};
	return {
		getInstance: function () {
			if (!instance) {
				instance = init();
			}
			return instance;
		}
	}
})();
```

> Singleton 的存在表明系统的模块要么是紧密耦合，要么是其逻辑过于分散
在代码库的多个部分。