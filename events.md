##JavaScript 事件
###事件是什么？
*JavaScript* 与 *HTML* 的交互是通过事件来处理的，当用户或浏览器操纵页面时。事件就会发生。  

当页面加载时,这是一个事件。当用户单击一个按钮,点击,是一个事件。另一个例子的事件就像按任何键,关闭窗口,调整窗口等。  

开发人员可以使用这些事件来执行 *JavaScript* 编码的响应,如导致按钮关闭窗口,信息显示给用户,数据验证,和任何其他类型的反应的发生。
事件都是文档对象模型（*DOM*）三级的一部分，并且每个HTML元素有一定的事件可以触发 *JavaScript* 代码。  

请通过这个小教程为更好地理解 *HTML* 事件参考。这里我们将看到一些例子来理解事件和 *JavaScript* 之间的关系:  

### onclick 事件类型:
这是最常用的事件类型,当用户点击鼠标左按钮。你可以把你的验证、警告等反对这个事件类型。  

###例子：  

    <html>
    <head>
    <script type="text/javascript">
    <!--
    function sayHello() {
       alert("Hello World")
    }
    //-->
    </script>
    </head>
    <body>
    <input type="button" onclick="sayHello()" value="Say Hello" />
    </body>
    </html>  

它将产生以下结果,然后当你点击你好按钮 *onclick* 事件将发生,将触发     *sayHello()* 函数。

<html>
<head>
<script type="text/javascript">
<!--
function sayHello() {
   alert("Hello World")
}
//-->
</script>
</head>
<body>
<input type="button" onclick="sayHello()" value="Say Hello" />
</body>
</html>

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_4)。
### onsubmit 事件类型:  

另一个最重要的是 *onsubmit* 事件类型。这个事件发生在您尝试提交一个表单。所以你可以用此事件类型进行表单验证。  

下面一个简单简单的例子显示其用法。我们在这里调用 *validate() *函数之前提交表单数据到网络服务器。如果 *validate()* 函数返回 *true* 表单将提交否则不会提交数据。  
###例子：  

    <html>
    <head>
    <script type="text/javascript">
    <!--
    function validation() {
       all validation goes here
       .........
       return either true or false
    }
    //-->
    </script>
    </head>
    <body>
    <form method="POST" action="t.cgi" onsubmit="return validate()">
    .......
    <input type="submit" value="Submit" />
    </form>
    </body>
    </html>  
### onmouseover 和 onmouseout :  

这两个事件类型将会帮助你创建好良好的图像效果和文本事件。*onmouseover* 事件发生时,当你把你的鼠标在任何元素上时， *onmouseover* 事件发生。当你把鼠标从该元素移开时，*onmouseout* 事件发生。
###例子：  

下面的例子显示了一个部位如何反应当我们把鼠标在这个部位上：   

    <html>
    <head>
    <script type="text/javascript">
    <!--
    function over() {
       alert("Mouse Over");
    }
    function out() {
       alert("Mouse Out");
    }
    //-->
    </script>
    </head>
    <body>
    <div onmouseover="over()" onmouseout="out()">
    <h2> This is inside the division </h2>
    </div>
    </body>
    </html>  
    
为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_26)。  

你可以改变不同的图像使用这两种事件类型或您可以创建帮助气框,来帮助你的用户。  

###HTML 4标准事件
标准的 *HTML 4* 事件被列在这里,供您参考。执行以下脚本显示一个Javascript函数。
<table border="">
<tr>
<th>Event</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>onchange</td>
<td>script</td>
<td>Script runs when the element changes</td>
</tr>
<tr>
<td>onsubmit1</td>
<td>script</td>
<td>Script runs when the form is submitted</td>
</tr>
<tr>
<td>onreset</td>
<td>script</td>
<td>Script runs when the form is reset</td>
</tr>
<tr>
<td>onselect</td>
<td>script</td>
<td>Script runs when the element is selected</td>
</tr>
<tr>
<td>onblur</td>
<td>script</td>
<td>Script runs when the element loses focus</td>
</tr>
<tr>
<td>onfocus</td>
<td>script</td>
<td>Script runs when the element gets focus</td>
</tr><tr>
<td>onkeydown</td>
<td>script</td>
<td>Script runs when key is pressed</td>
</tr>
<tr>
<td>onkeypress</td>
<td>script</td>
<td>Script runs when key is pressed and released</td>
</tr>
<tr>
<td>onkeyup</td>
<td>script</td>
<td>Script runs when key is released</td>
</tr>
<td>onclick</td>
<td>script</td>
<td>Script runs when a mouse click</td>
</tr>
<td>ondblclick</td>
<td>script</td>
<td>Script runs when a mouse double-click</td>
</tr>
<td>onmousedown</td>
<td>script</td>
<td>Script runs when mouse button is pressed</td>
</tr>
<td>onmousemove</td>
<td>script</td>
<td>Script runs when mouse pointer moves</td>
</tr>
<td>onmouseout</td>
<td>script</td>
<td>Script runs when mouse pointer moves out of an element</td>
</tr>
<td>onmouseover</td>
<td>script</td>
<td>Script runs when mouse pointer moves over an element</td>
</tr>
<td>onmouseup</td>
<td>script</td>
<td>Script runs when mouse button is released</td>
</tr>
</table>  


