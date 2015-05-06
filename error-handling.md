##JavaScript - 错误 & 异常处理##

程序中存在三种错误： (a) 语法错误 (b) 运行期错误 (c) 逻辑错误:

###语法错误:###

语法错误同样也被称为解析错误，对于传统的编程语言，该错误出现先编译的时候，对于 JavaScript 该错误出现在解释时期。
例如，下面的代码会引起语法错误，因为在一行中缺少一个圆括号：

	<script type="text/javascript">
	<!--
	window.print(;
	//-->
	</script>

当在 JavaScript 中出现了语法错误的时候，仅仅只是在同一个包含该语法错误的进程才会受到影响，其他的进程中的代码执行不会受到影响，尽管他们依赖的代码中包含错误。

###运行期错误:###

运行期错误也被称为异常，通常在编译或者解释之后运行时会出现。
例如，下面的代码会造成运行期错误，因为它试图调用一个不存在的方法：

	<script type="text/javascript">
	<!--
	window.printme();
	//-->
	</script>

异常出现时会影响进程创建时的正常执行，但是允许对于其他的 JavaScript 进程则可以继续正常执行。

###逻辑错误: ###

逻辑错误是最难被追踪的错误类型。这些错误并不是语法或者运行时错误造成的， 而是由于你在程序运行的逻辑上出现错误，从而导致你的脚本程序并不能得到你想要的结果。

你并不能捕获这些错误，因为它取决于你的业务逻辑需求，你想要在你的程序中实现怎样的逻辑处理。

### try...catch...finally 语句：###

JavaScript 的最新版本中添加了异常处理的功能。它实现了 try...catch...finally 结构和 throw 操作用来处理异常。
你可以捕获程序员和运行期产生的异常，但是对于用户不能捕获 JavaScript 的语法错误。
下面是 try...catch...finally 语法块:

	<script type="text/javascript">
	<!--
	try {
    	// Code to run
    	[break;]
	} catch ( e ) {
    	// Code to run if an exception occurs
    	[break;]
	}[ finally {
    	// Code that is always executed regardless of 
    	// an exception occurring
	}]
	//-->
	</script>

**try** 语句块后面必须跟着一个 **catch** 语句块或者一个 **finally** 语句块(或者同时包含他俩的一个语句块)。当在 **try** 语句块内部产生了一个异常，这个异常就会被赋值给 **e**，接着 **catch** 语句块被执行。而可选的 **finally** 语句块在 try/catch 之后一定会被执行。

###例子：###

如下是一个例子，我们尝试调用一个不存在的方法，这个会导致异常的产生。我们首先看下没有 **try...catch** 语句时运行情况：

	<html>
	<head>
	<script type="text/javascript">
	<!--
	function myFunc()
	{
	   var a = 100;
	
	   alert("Value of variable a is : " + a );
 
	}
	//-->
	</script>
	</head>
	<body>
	<p>Click the following to see the result:</p>
	<form>
	<input type="button" value="Click Me" onclick="myFunc();" />
	</form>
	</body>
	</html>

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_35)。

接下来利用 **try...catch** 语句尝试去捕获程序的异常，并且给用户提示一个友好的消息。如果你不想让用户看见这个错误，你也可以不让这个消息产生。

	<html>
	<head>
	<script type="text/javascript">
	<!--
	function myFunc()
	{
	   var a = 100;
	   
		try {
      		alert("Value of variable a is : " + a );
		} catch ( e ) {
      		alert("Error: " + e.description );
	  	}
	}
	//-->
	</script>
	</head>
	<body>
	<p>Click the following to see the result:</p>
	<form>
	<input type="button" value="Click Me" onclick="myFunc();" />
	</form>
	</body>
	</html>

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_36)。

你还可以使用 **finally** 语句，它会在 try/catch 语句之后必定执行。如下例子所示：

	<html>
	<head>
	<script type="text/javascript">
	<!--
	function myFunc()
	{
		var a = 100;
		try {
      		alert("Value of variable a is : " + a );
		}catch ( e ) {
     		alert("Error: " + e.description );
		}finally {
      		alert("Finally block will always execute!" );
		}
	}
	//-->
	</script>
	</head>
	<body>
	<p>Click the following to see the result:</p>
	<form>
	<input type="button" value="Click Me" onclick="myFunc();" />
	</form>
	</body>
	</html>

为了更好的理解此处的内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_37)。

###throw 语句：###

你可以使用 **throw** 语句产生一个内置的异常或者你自己定制的异常。之后这些异常可以被捕获，而且捕获后你可以采取合适的操作。

下面的是一个例子，展示如何使用 **throw** 语句。

	<html>
	<head>
	<script type="text/javascript">
	<!--
	function myFunc()
	{
		var a = 100;
		var b = 0;

		try{
	      if ( b == 0 ){
	         throw( "Divide by zero error." ); 
	      }else{
	         var c = a / b;
	      }
		}catch ( e ) {
      		alert("Error: " + e );
		}
	}
	//-->
	</script>
	</head>
	<body>
	<p>Click the following to see the result:</p>
	<form>
	<input type="button" value="Click Me" onclick="myFunc();" />
	</form>
	</body>
	</html>

为了更好的理解此处的内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_38)。

你可以在一个函数里面利用字符串，整型，布尔类型或者一个对象引起异常，接着你可以在同一个方法里面捕获这个异常，或者在其他的函数里面利用 **try...catch** 语句块捕获异常。

###onerror() 方法###

**onerror** 事件句柄是 JavaScript 中添加的第一个为了方便错误处理的特性。无论任何时候在网页中产生了异常，窗口对象就会触发 **error** 事件。例如：

	<html>
	<head>
	<script type="text/javascript">	
	<!--
	window.onerror = function () {
	   alert("An error occurred.");
	}
	//-->
	</script>
	</head>
	<body>
	<p>Click the following to see the result:</p>
	<form>
	<input type="button" value="Click Me" onclick="myFunc();" />
	</form>
	</body>
	</html>

为了更好的理解此处的内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_39)。

**onerror** 事件句柄提供了三个信息用来准确的表示错误的特性：

- 错误消息。 浏览器显示给定错误的相关信息。
- URL。 错误出现的文件。
- 行数。 在指定的 URL 中造成错误的行数。

如下是一个例子显示如何得到上面的那些信息。

	<html>
	<head>
	<script type="text/javascript">
	<!--
	window.onerror = function (msg, url, line) {
		alert("Message : " + msg );
		alert("url : " + url );
		alert("Line number : " + line );
	}
	//-->
	</script>
	</head>
	<body>
	<p>Click the following to see the result:</p>
	<form>
	<input type="button" value="Click Me" onclick="myFunc();" />
	</form>
	</body>
	</html>

你可以用任何你认为更好的方式来显示得到的信息。

为了更好的理解此处的内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_40)。

你可以使用 **onerror** 方法来显示一个错误消息，以免在加载图片时出现任何的问题：

	<img src="myimage.gif"
		onerror="alert('An error occurred loading the image.')" />

如果程序中产生错误，你可以在很多的 HTML 标签中使用 **onerror** 来显示合适的消息。