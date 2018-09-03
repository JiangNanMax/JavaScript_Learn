# 09-JavaScript基础-数据类型转换

### 数据类型转换

* 什么是数据类型转换

	* 将一个数据类型转换为其他的数据类型，比如：将String转换为Number类型，将Number类型转换为Boolean类型... ...

* toString()

	* 将其他类型的数据转换为字符串类型

		> var num = 12306;<br>
		var str = num.toString();<br>
		console.log(str); &emsp;&emsp;//&emsp;&emsp;12306<br>
		console.log(typeof str); &emsp;&emsp;//&emsp;&emsp;string<br>
		<br>
		var num1 = true;<br>
		var str1 = num1.toString();<br>
		console.log(str1); &emsp;&emsp;//&emsp;&emsp;true<br>
		console.log(typeof str1) &emsp;&emsp;//&emsp;&emsp;string<br>
		
	* 注意：null和undefined没有toString()方法，如果强行调用，则会报错

		> var num2 = undefined;<br>
		var str2 = num2.toString() &emsp;&emsp;//&emsp;&emsp;报错<br>
		<br>
		var num3 = null;<br>
		var str3 = num3.toString(); &emsp;&emsp;//&emsp;&emsp;	报错<br>
		<br>
		var num4 = NaN;<br>
		vat str4 = num4.toString();<br>
		console.log(str4); &emsp;&emsp;//&emsp;&emsp;NaN<br>
		console.log(typeof str4); &emsp;&emsp;//&emsp;&emsp;string<br>
		
	* toString()不会影响到原变量，它会将转换的结果返回

		> var num5 = 10;<br>
		var str5 = num5.toString();<br>
		console.log(typeof num5); &emsp;&emsp;//&emsp;&emsp;number<br>
		console.log(typeof str5); &emsp;&emsp;//&emsp;&emsp;string<br>
		
* String()函数

	* 有的时候，某些值并没有toString()方法，这个时候可以使用String()。比如：undefined和null。

* +

	* 任何数据和+连接到一起都会转换为字符串，其内部实现原理和String()函数一样

		