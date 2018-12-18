# 11-JavaScript基础-算术运算符

### 加法运算

* 格式：Number1 + Number2

* 非Number类型的值进行运算时，会将这些值转化为Number然后再进行运算

* 任何值和NaN做运算的结果都是NaN

* 任何值和字符串做加法运算，都会先转化为字符串，然后再和字符串做拼串的操作

### 减法运算

* 格式：Number1 - Number2

* 非Number类型的值进行运算时，会将这些值转化为Number然后再进行运算

* 任何值和NaN做运算的结果都是NaN

* 字符串做减法运算会转化为Number

```
	var result = 2 - "1";
	console.log(result); //1
	var result = "2" - "1";
	console.log(result); //1
```

### 乘法运算

* 格式：Number1 + Number2

* 其它规律和减法一样

	* 非Number类型的值进行运算时，会将这些值转化为Number然后再进行运算

	* 任何值和NaN做运算的结果都是NaN

	* 字符串做乘法运算会转化为Number

### 除法运算

* 格式：Number1 / Number2

* 其它规律和减法一样

	* 非Number类型的值进行运算时，会将这些值转化为Number然后再进行运算

	* 任何值和NaN做运算的结果都是NaN

	* 字符串做除法运算会转化为Number

### 取余运算

* 格式：Number1 % Number2

* 其它规律和减法一样

	* 非Number类型的值进行运算时，会将这些值转化为Number然后再进行运算

	* 任何值和NaN做运算的结果都是NaN

	* 字符串做取余运算会转化为Number

* m%n求余，相当于m/n获取余数

	* n等于0，返回NaN

	* m等于0，结果为0

	* m>n，正常求余

	* m<n，结果为m