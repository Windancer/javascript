##JavaScript 动画###

你可以利用 JavaScript 创造一些复杂的运动，包括下面但不限于下面的：

- 烟花式
- 淡出效果
- 旋转进入或者旋转推出
- 整个页面进入或者整个页面出去
- 对象移动

你如果对这个感兴趣，你可以查看基于 JavaScript 的动画库 [Script.Aculo.us](http://www.tutorialspoint.com/script.aculo.us/scriptaculous_effects.htm)。

这个教程将讲解如何利用 JavaScript 创建一些基本的运动。

JavaScript 可以用来移动一些文档对象模型元素(<img />, <div> 或者其他的 HTML 元素)在页面附近，这个是通过一些逻辑等式或者函数来决定的。

JavaScript 提供如下的几种比较常用的函数来进行动画编程。

- **setTimeout(function, duration)**： 这个函数在规定的时间 _duration_ 到达时，会调用参数中的函数 _function_。
- **setInterval(function, duration)**： 这个方法调用了之后会清除所有 setTimeout() 函数设定的计时器。

JavaScript 能够设置一系列文档模型对象的属性值，包括该对象在屏幕中的位置。你可以通过设置 _top_ 和 _left_ 等对象的属性值，从而让该对象放在屏幕中任何位置。如下是该语法的一个简单例子：

	// Set distance from left edge of the screen.
	object.style.left = distance in pixels or points; 

	or
	// Set distance from top edge of the screen.
	object.style.top = distance in pixels or points; 

###手动动画###

让我们利用文档对象模型的对象的属性值实现一个简单的动画，JavaScript 的函数如下：

	<html>
	<head>
	<title>JavaScript Animation</title>
	<script type="text/javascript">
	<!--
	var imgObj = null;
	function init(){
		imgObj = document.getElementById('myImage');
		imgObj.style.position= 'relative'; 
	imgObj.style.left = '0px'; 
	}
	function moveRight(){
		imgObj.style.left = parseInt(imgObj.style.left) + 10 + 'px';
	}
	window.onload =init;
	//-->
	</script>
	</head>
	<body>
	<form>
	<img id="myImage" src="/images/html.gif" />
	<p>Click button below to move the image to right</p>
	<input type="button" value="Click Me" onclick="moveRight();" />
	</form>
	</body>
	</html>

如下是对上面例子的解释：

- 我们利用 JavaScript 的函数 _getElementById()_ 得到了文档对象模型对象，接着把它赋值给一个全局变量 _imgObj_。
- 我们定义了一个初始化函数 _init()_ 用来初始化 _imgObj_ 对象,初始化时设置了该对象的 _position_ 和 _left_ 属性的值。
- 初始化函数在网页窗口加载的时候被调用。
- 最后，我们调用 _moveRight()_ 函数增加该对象到左边边界的距离为 10 个像素点。你也可以设置该对象到左边的距离为负值。

为了更好理解此处的内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_44)。

###自动动画###

在上面的例子中我们已经看到如何让一张图片在每次点击之后向右移动。我们可以通过利用 JavaScript 中的函数 _setTimeout()_ 让它自动执行这个操作：

	<html>
	<head>
	<title>JavaScript Animation</title>
	<script type="text/javascript">
	<!--
	var imgObj = null;
	var animate ;
	function init(){
	imgObj = document.getElementById('myImage');
	imgObj.style.position= 'relative'; 
	imgObj.style.left = '0px'; 
	}
	function moveRight(){
	imgObj.style.left = parseInt(imgObj.style.left) + 10 + 'px';
	animate = setTimeout(moveRight,20); // call moveRight in 20msec
	}
	function stop(){
	clearTimeout(animate);
	imgObj.style.left = '0px'; 
	}
	window.onload =init;
	//-->
	</script>
	</head>
	<body>
	<form>
	<img id="myImage" src="/images/html.gif" />
	<p>Click the buttons below to handle animation</p>
	<input type="button" value="Start" onclick="moveRight();" />
	<input type="button" value="Stop" onclick="stop();" />
	</form>
	</body>
	</html>

这里我们增加了一些新的知识：

- _moveRight()_ 函数通过调用 _setTimeout()_ 函数设置 _imgObj_ 对象的位置。
- 我们添加了一个新的函数 _stop()_ ，它的作用是用来清除 _setTimeout()_ 函数设置的计时器和让文档对象处于它的初始位置。

为了更好的理解此处的内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_45)。

###伴随鼠标事件的翻转###

如下是一个简单的例子演示由鼠标事件引起的图片翻转：

	<html>
	<head>
	<title>Rollover with a Mouse Events</title>
	<script type="text/javascript">
	<!--
	if(document.images){
		var image1 = new Image();      // Preload an image
    	image1.src = "/images/html.gif";
    	var image2 = new Image();      // Preload second image
    	image2.src = "/images/http.gif";
	}
	//-->
	</script>
	</head>
	<body>
	<p>Move your mouse over the image to see the result</p>
	<a href="#" onMouseOver="document.myImage.src=image2.src;"
            onMouseOut="document.myImage.src=image1.src;">
	<img name="myImage" src="/images/html.gif" />
	</a>
	</body>
	</html>

让我们来看看这里的不同点：

- 在加载这个网页的时候，if 语句是否存在图片对象。如果没有有效的图片对象，那么下面的语句块不会被执行。
- Image() 构造方法创建和预加载一个新的图片对象称为 image1。
- src 属性值被赋值为外部图片文件的路径名称，即是 /images/html.gif。
- 同样的方式，我们创建了 image2对象，并且给它赋值为 /images/http.gif。
- 符号 # 禁用链接，这样浏览器中点击该链接就不会发生跳转。这个链接表示的是一个图片。
- _onMouseOver_ 事件句柄在用户的鼠标移动到链接上时会被触发，同样，用户鼠标离开图片链接时会触发 _onMouseOut_ 事件句柄。
- 当鼠标移动到图片上时，HTTP 上的图片就会从第一个变到第二个。用鼠标离开图片时，最开始的那副图片就会被显示。
- 当鼠标从图片链接上离开时，初始的 html.gif 图片会再次出现在屏幕上面。

为了更好理解此处的内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_46)。