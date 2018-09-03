# 02-JavaScript基础-书写格式

### JavaScript的语法规范

* JavaScript有三种书写格式，分别是“行内式”、“页内式”、“外链式”
	* 行内式

		```
		<button onclick = "alert('今天天气很好! ');">今天天气很好！</button>
		```
		* 行内式注意点
		
			* JS内使用单引号		
	
	* 页内式
	
		```
			<body>
				<script type = "text/javascript">
					alert("今天天气很好！");
				</script>
			</body>
		```
	
		* 页内式注意点

			* script标签中的js代码一般写在文档的尾部
			
			* 网页是从上至下加载，而js代码通常是给标签添加交互（操作元素），所以需要先加载HTML，否则如果执行js代码时HTML还未被加载，那么js代码将无法添加交互（操作元素）

			* HTML页面中出现script标签后，就会让页面暂停，等待脚本的解析和执行。无论当前脚本是内嵌式还是外链式，页面的下载和渲染都必须停下来，等待脚本的执行完成才能继续。所以如果把js代码写在head中，那么js代码执行完毕之前后续网页无法被加载。

	* 外链式

		```
		<script type = "text/javascript" src = "js/index.js">\</script>
		```
		
		* 外链式注意点

			* 外链式的script代码块中不能编写js代码，即使写了也不会执行
			
				```
				<script type = "text/javascript" src = "js/index.js">
					alert("今天天气很好！”); //不会被执行
				</script>
				```
				
			* 由于每次加载外链式的js文件都会发送一次请求，这样非常消耗性能，所以在企业开发中推荐将多个js文件打包成为一个js文件，以提升网页的性能和加载速度。
		
	

