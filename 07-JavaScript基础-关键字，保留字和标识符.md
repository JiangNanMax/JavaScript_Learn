# 07-JavaScript基础-关键字，保留字和标识符

### 关键字和保留字

* 什么是关键字？
	
	* JavaScript语言用于程序控制或执行特定操作的英语单词；<br>

	* 它们是被JavaScript语言赋予了特殊含义的英文单词；

		* 好比现实生活中除夕、中秋、国庆对于我们有特殊含义一样，在JavaScript也有一些对于JavaScript有特殊含义的单词，这些单词我们称之为关键字。
		
	* 关键字不能用作变量名、函数名；
	* 关键字严格区分大小写，比如：void和Void前者是关键字，后者不是
	* 汇总如下：
	
		|||||
		| :------ | :------ | :------ | :------ |
		| break | do | instanceof | typeof |
		| case | else | new | var |
		| catch | finally | return | void |
		| continue | for | switch | while |
		| debugger | function | this | with |
		| default | if | throw | delete |
		| in | try |  |  |
		
* 什么是保留字？

	* JavaScript预留的关键字，它们虽然现在还没有作为关键字，但在以后的升级版本中有可能作为关键字

		|||||
		| :------ | :------ | :------ | :------ |
		| class | enum | extends | super |
		| const | export | import |  |

### 标识符
* 什么是标识符？

	* 在JS中所有的可以由我们自主命名的都可以称为是标识符<br>

	* 比如变量名、函数名、属性名都属于标识符

		* 例如：var name; ， 这里的name就是标识符
		
	* 命名一个标识符时需要遵守如下的规则：<br>

		* 标识符中可以含有字母、数字、下划线_、$符号<br>

		* 标识符不能以数字开头

		* 标识符不能是ES中的关键字或保留字
		* 严格区分大小写，比如name和Name是2个不同的标识符
		* 标识符一般都采用驼峰命名法

			* 首字母小写，每个单词的开头字母大写，其余字母小写<br>
			helloWorld xxxYyyZzz
			
		* JS底层保存标识符时实际上是采用的Unicode编码，所以理论上讲，所有的utf-8中含有的内容都可以作为标识符