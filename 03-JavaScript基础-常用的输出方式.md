# 03-JavaScript基础-常用的输出方式

### JavaScript初体验(一)

* 使用JavaScript在网页中输出一句话

	* 方式一

		在网页中弹出显示框，显示信息
		
		```
		<script>
			alert("Hello, JavaScript!");
		</script>
		```
		
	* 方式二
	
		在控制台输出消息，一般用来调试程序
		
		```
		<script>
		console.log("Hello, JavaScript!");
		console.warn("警告输出!");
		console.error("错误输出!");
		<script>
		```
		
	* 方式三

		在网页中弹出输入框，一般用于接收用户输入的信息
		
		```
		<script>
		prompt("Hello, JavaScript!");
		</script>
		```
		
	* 方式四

		在网页中弹出提示框，显示信息，该方法一般与if判断语句结合使用
		
		```
		<script>
		confirm("Hello, JavaScript!");
		</script>
		```
		
	
		
		

