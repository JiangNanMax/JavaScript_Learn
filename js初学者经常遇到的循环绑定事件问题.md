# js初学者经常遇到的循环绑定事件问题

* js循环绑定事件

	* 在编写JS代码的时候，我们经常会遇到要对一系列元素进行事件绑定的情况，然后就会理所当然的开一个for循环，对元素的事件进行赋值等操作，最后运行的效果却不是希望有的样子，事件的响应只能和最后一个元素一样，怎么肥四？？？

	* 下面给出错误的代码：

	```
	<!DOCTYPE html>
	<html lang="en">
	<head>
    	<meta charset="UTF-8">
    	<title>Title</title>
	</head>
	<body>
    	<button>btn1</button>
    	<button>btn2</button>
    	<button>btn3</button>
    	<button>btn4</button>
    	<button>btn5</button>

    <script>
        window.onload = function () {
            var btnList = document.getElementsByTagName("button");

            //console.log(btnList);

            for (var i=0; i<btnList.length; i++){
                btnList[i].onclick = function () {
                    console.log(i);
                }
            }
        }
    </script>

	</body>
	</html>
	```
	
	* 如此的话，不管点击哪个按钮，你会发现输出的都是5。因为js的函数是触发时调用的，绑定事件的时候i并没有被传入执行函数里。这里的onclick函数中的变量i指向的内存地址，在循环结束后变成了5，所以所有的btn在点击后都输出5。

* 解决方法

	* 这里给出我使用的两种解决方法，第一种相对容易理解，第二种就是闭包的方法，就需要理解闭包的思想（下一篇博客再对闭包做一下总结）。

	* 第一种方法

	```
	<!DOCTYPE html>
	<html lang="en">
	<head>
    	<meta charset="UTF-8">
    	<title>Title</title>
	</head>
	<body>
    	<button>btn1</button>
    	<button>btn2</button>
    	<button>btn3</button>
    	<button>btn4</button>
    	<button>btn5</button>

    <script>
        window.onload = function () {
            var btnList = document.getElementsByTagName("button");

            //console.log(btnList);

            for (var i=0; i<btnList.length; i++){
                var btnTemp = btnList[i];
                btnTemp.index = i;  //给该元素添加一个index属性来存储i

                btnTemp.onclick = function () {
                    console.log(this.index);
                }
            }
        }
    </script>

	</body>
	</html>
	```
	
	这个方法就是通过给每个元素添加一个属性来存储i值来实现的。
	
	* 第二种方法

	```
	<!DOCTYPE html>
	<html lang="en">
	<head>
    	<meta charset="UTF-8">
    	<title>Title</title>
	</head>
	<body>
    	<button>btn1</button>
    	<button>btn2</button>
    	<button>btn3</button>
    	<button>btn4</button>
    	<button>btn5</button>

    <script>
        window.onload = function () {
            var btnList = document.getElementsByTagName("button");

            //console.log(btnList);

            for (var i=0; i<btnList.length; i++){
                (function (i) {
                    btnList[i].onclick = function(){
                        console.log(i);
                    }
                })(i);
            }
        }
    </script>

	</body>
	</html>
	```
	闭包的思想。
	

