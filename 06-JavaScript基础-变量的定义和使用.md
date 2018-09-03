# 06-JavaScript基础-变量的定义和使用

### JS中变量的定义

* 定义变量的目的

	* 在内存中分配一块存储空间给变量，方便以后存储数据。

* 如何定义变量？

	* 定义变量（声明变量），任何变量在使用之前，必须先进行定义
	
	* 如果定义了多个变量，就会为这多个变量分别分配不同的存储空间
	* var 变量名称;
		
		```
			var name;
			var name, age, sex;
		```
		
* 如何使用变量？
	* 使用变量就是往变量里面放入内容或者取出变量中存储的内容
	
	* 往变量中存储内容
	
		```
			var name;
			name = "JiangNanMax";
		```
		
		* 注意：
			1. = 为赋值符号，不是我们理解的数学中的“等号”，它是JavaScript语言中的赋值运算符，作用是将右边的常量"JiangNanMax"赋值给左边的变量name
			
			2. 赋值的时候 = 号的左侧必须是变量
			3. = 左右两边各加一个空格

* 如何进行变量初始化

	* 变量第一次赋值，可以称为“初始化”

		* 先定义，后初始化
		
			```
				var name;
				name = "JiangNanMax";
			```
			
		* 定义的同时尽心初始化

			```
				var name = "JiangNanMax";
			```
			
		* 其他表现形式

			```
				// 部分初始化
				var num1, num2, num3 = 100;
				//完全初始化
				var num1 = num2 = num3 = 100;
			```
			
		* 如果定义后没有初始化

			```
				var num;
				console.log(num); // undefined
			```
			
* 如何查看变量的值？

	```
		var name = "JiangNanMax";
		console.log(name);
	```
	
* 如何修改变量值？

	* 通过等号( = )重新赋值即可，每次赋值都会覆盖原来的值

		```
			var name = "JiangNanMax";
			name = "YangMan";
			console.log(name);
		```
		
* 变量之间的值传递

	* 可以将一个变量的值赋给另一个变量
	
		```
			var num1 = 100;
			var num2 = num1;
			console.log(num2);	
		```	
		
		
		
		
		
		
		
		
		
		
		
		

