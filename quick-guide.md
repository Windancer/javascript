# 快速指南 

## JavaScript 是什么？ 

JavaScript 具有如下特征：  
- 轻量级的解释型（代码不需要经过预编译）可编程语言。  
- 用于网络应用开发的脚本语言。  
- 可以与 JAVA、HTML 语言互补集成。  
- 开放且跨平台。  

## JavaScript 语法 


一段 JavaScript 脚本由包含在网页页面中 `<script>... </script>` 标签内的 JavaScript 语句组成。  

编程人员可以随意将由 `<script>` 标签包含着的 JavaScript 脚本置于网页的任意位置，但是通常都会放在 `<head>` 标签内。  

`<script>` 标记用来让浏览器明白这个标签之间的语句需要作为脚本来解释。所以，JavaScript 脚本可以简单的按照如下形势来表示：  


    <script ...>
      JavaScript code
    </script

`<script>` 标签有两个很重要的属性：  
- 语言（language）：这个属性指定你正在使用什么脚本语言。一般来说,指的都是 javascript。尽管最近版本的HTML(XHTML 及后续版本)会逐步不再使用这个属性。     
- 类型（type）： 该属性用于表明脚本语言类别的。通常应该设置为“*text/javascript*”。  

所以 JavaScript 片段是如下形式：

    <script language="javascript" type="text/javascript">
      JavaScript code
    </script>


## 尝试写第一个 JavaScript 脚本  

我们试着利用 JavaScript 脚本写一个打印 “Hello word” 的功能。  


    <html>
    <body>
    <script language="javascript" type="text/javascript">
    <!--
       document.write("Hello World!")
    //-->
    </script>
    </body>
    </html>

上面的脚本会显示如下结果：  

    Hello World!

## 空格和换行符

JavaScript编译器会忽略掉脚本中的所有空白、缩进符、换行符。  

因此，程序员可以在脚本中自用使用空格、缩进和换行符，这样程序员就可以随意缩进格式化程序格式,以便代码更易于阅读和理解。  

## 分号是可选的 ##

与 C、C++ 和 JAVA一样，通常 JavaScript 语句以分号结尾。但是， JavaScript 允许在每行只有一句脚本的情况下省略分号。比如，下方的脚本就是可以省略分号的：  

    <script language="javascript" type="text/javascript">
    <!--
      var1 = 10
      var2 = 20
    //-->
    </script

但是一行中存在多个脚本语句时，分号是不能省略的，比如：  


    <script language="javascript" type="text/javascript">
    <!--
      var1 = 10; var2 = 20;
    //-->
    </script>

**注意：**使用分号是一个比较实用的编程习惯  

## 区分大小写 


JavaScript是一门大小写敏感的语言。这意味着关键词、变量、函数名及其他任何标识符在输入时都要保持一样的书写格式。  

所以，*Time*，*TIme* 和 *TIME* 在 JavaScript 中表示不同的意思。  

**注意：**在编写JavaScript脚本时一定要注意变量和函数名的书写。  

## 注释 


JavaScript 同样支持 C 和 C++ 那样的注释方式：  

- 任何以 “//” 开头的行均被认为是注释内容而被编译器忽略掉。  
- 任何以“/*”开头且以“*/” 结尾的内容均被视为注释内容，且这样的内容可以是多行的。  
- JavaScript 也识别 HTML 格式的注释开始标识"<!--"。它视该方式为单行注释方式，和//一样的效果。  
- HTML 注释结尾符“-->”不会被JavaScript识别，应该书写成“//-->”。  

## JavaScript脚本应置于HTML文件的何处 

在 HTML 文件中何处书写 JavaScript 脚本是非常灵活的。但是，通常情况下都会将脚本书写在 HTML 文件中的如下位置内：  

- `<head>...</head>`内  
- `<body>...</body>`内  
- `<body>...</body>`和`<head>...</head>`同时书写  
- 以外部文件的方式包含在`<head>...</head>`内  

## 数据类型 

JavaScript中可以市容下述三种数据类型：

- 数值类型：比如123,120.50等  
- 字符串类型：比如“This text string”  
- 布尔类型：比如true or false
  
JavaScript也支持另外两个常用类型：null和undefined，这两个类型均仅限定一个单一的值。  

## JavaScript变量

和其他可编程语言相同，JavaScript也有“变量”的概念。“变量”可以认为是有名字的容器。你可以将数据置于这些容器中，然后通过容器的名称就可以知道数据的类型。  
值得注意的是，在JavaScript编程过程中，必须先声明一个变量，这个变量才能被使用。  
此外，变量是通过“var”来声明的，例子如下：  

    <script type="text/javascript">
    <!--
    var money;
    var name;
    //-->
    </script>


## JavaScript变量作用域

一个变量的作用域就是该变量定义后在程序中的作用范围。JavaScript变量有两个变量作用域。  
    1.	全局变量：全局变量具有全部整体范围的作用域，这意味着它可以再JavaScript代码任何地方定义。  
    2.	局部变量：局部变量仅在定义它的函数体内可以访问到。函数参数对于函数来说就是局部变量。


### JavaScript变量名称

JavaScript中变量的命名规则如下：
- 1.	不能使用JavaScript中的保留关键字来命名变量。这些保留关键字会在下一节中介绍。比如break 或 boolean，这些命名变量是无效的。
- 2.	JavaScript变量名称不能以数字（0-9）开头，只能以字母或下划线来命名变量。比如123test就是无效的变量名。但是，_123就是有效的变量名。
- 3.	JavaScript变量名称对大小写敏感。比如，Name和name是两个不同的变量。

###JavaScript保留的关键字

下面是JavaScript中的保留关键字。他们不能用来命名JavaScript中的变量、行数、方法、循环标签或任何对象名称。  
  
<table>
   <tr>
      <td>abstract</td>
      <td>else</td>
      <td>instanceof</td>
      <td>switch</td>
   </tr>
   <tr>
      <td>boolean</td>
      <td>enum</td>
      <td>int</td>
      <td>synchronized</td>
   </tr>
   <tr>
      <td>break</td>
      <td>export</td>
      <td>interface</td>
      <td>this</td>
   </tr>
   <tr>
      <td>byte</td>
      <td>extends</td>
      <td>long</td>
      <td>throw</td>
   </tr>
   <tr>
      <td>case</td>
      <td>FALSE</td>
      <td>native</td>
      <td>throws</td>
   </tr>
   <tr>
      <td>catch</td>
      <td>final</td>
      <td>new</td>
      <td>transient</td>
   </tr>
   <tr>
      <td>char</td>
      <td>finally</td>
      <td>null</td>
      <td>TRUE</td>
   </tr>
   <tr>
      <td>class</td>
      <td>float</td>
      <td>package</td>
      <td>try</td>
   </tr>
   <tr>
      <td>const</td>
      <td>for</td>
      <td>private</td>
      <td>typeof</td>
   </tr>
   <tr>
      <td>continue</td>
      <td>function</td>
      <td>protected</td>
      <td>var</td>
   </tr>
   <tr>
      <td>debugger</td>
      <td>goto</td>
      <td>public</td>
      <td>void</td>
   </tr>
   <tr>
      <td>default</td>
      <td>if</td>
      <td>return</td>
      <td>volatile</td>
   </tr>
   <tr>
      <td>delete</td>
      <td>implements</td>
      <td>short</td>
      <td>while</td>
   </tr>
   <tr>
      <td>do</td>
      <td>import</td>
      <td>static</td>
      <td>with</td>
   </tr>
   <tr>
      <td>double</td>
      <td>in</td>
      <td>super</td>
      <td></td>
   </tr>

</table>  

## 算数运算符 

JavaScript语言支持以下算术运算符 

给定 **A**=10，**B**=20，下面的表格解释了这些算术运算符：  

<table>
<tbody>
<tr>
<th>运算符</th>  <th>描述</th> <th>例子</th>
</tr>
<tr>
<td>+</td>
<td>两个运算数相加</td>
<td>A + B = 30</td>
</tr>
<tr>
<td>-</td>
<td>第一个运算数减去第二个运算数</td>
<td>A - B = -10</td>
</tr>
<tr>
<td>*</td>
<td>运算数相乘   </td>
<td>A * B = 200</td>
</tr>
<tr>
<td>/</td>
<td>分子除以分母</td>
<td>B / A = 2</td>
</tr>
<tr>
<td>%</td>
<td>模数运算符，整除后的余数</td>
<td>B % A = 0</td>
</tr>
<tr>
<td>++</td>
<td>增量运算符，整数值逐次加1</td>
<td>A++ = 11</td>
</tr>
<tr>
<td>--</td>
<td>减量运算符，整数值逐次减1</td>
<td>A-- = 9</td> </tr> 
</tbody>
</table>



## 比较运算符 

JavaScript语言支持以下比较运算符  

给定 **A**=10，**B**=20，下面的表格解释了这些比较运算符：  


<table>
<tbody>
<tr>
<th>运算符</th>
<th>描述</th>
<th>例子</th>
</tr>
<tr>
<td>==</td> <td>检查两个运算数的值是否相等，如果是，则结果为true</td> <td>A == B 为false</td>
</tr>
<tr>
<td>!=</td> <td>检查两个运算数的值是否相等，如果不相等，则结果为true    </td>
<td>A != B 为true</td>
</tr>
<tr>
<td>&gt;</td>  <td>检查左边运算数是否大于右边运算数，如果是，则结果为true </td>
<td>A &gt; B 为false</td>
</tr>
<tr>
<td>&lt;   </td>
<td>检查左边运算数是否小于右边运算数，如果是，则结果为true</td>
<td>   A &lt; B 为true</td>
</tr>
<tr>
<td>&gt;=</td> <td>检查左边运算数是否大于或者等于右边运算数，如果是，则结果为true</td>    <td>A &gt;= B 为false</td>
</tr>
<tr>
<td>&lt;=</td>
<td> 检查左边运算数是否小于或者等于运算数，如果是，则结果为true</td>  <td>A &lt;= B 为true</td>
</tr>
</tbody>
</table>

## 逻辑运算符 

JavaScript语言支持以下逻辑运算符 

给定 <strong>A=10，B=20</strong>，下面的表格解释了这些逻辑运算符  

<table>
<tbody>
<tr>
<th>运算符</th>  <th>描述</th> <th>例子</th>
</tr>
<tr>
<td>&amp;&amp;  </td>
<td>称为逻辑与运算符。如果两个运算数都非零，则结果为true。</td>
<td>   A &amp;&amp; B 为true</td>
</tr>
<tr>
<td>||  </td>
<td>称为逻辑或运算符。如果两个运算数中任何一个非零，则结果为true。</td>
<td>   A || B 为 true</td>
</tr>
<tr>
<td>!   </td>
<td>称为逻辑非运算符。用于改变运算数的逻辑状态。如果逻辑状态为true，则通过逻辑非运算符可以使逻辑状态变为false  </td>
<td>!(A &amp;&amp; B) 为false</td>
</tr>  
</tbody>
</table> 

## 按位运算符 

JavaScript语言支持以下逻辑运算符

给定 **A**=2，**B**=3，下面的表格解释了这些逻辑运算符 

<table>
<tbody>
<tr>
<th>运算符</th>
<th>描述</th>   <th>例子</th>
</tr>
<tr>
<td>&amp;   </td>
<td>称为按位与运算符。它对整型参数的每一个二进制位进行布尔与操作。</td>
<td> A &amp; B = 2 .</td>
</tr>
<tr>
<td>|   </td>
<td>称为按位或运算符。它对整型参数的每一个二进制位进行布尔或操作。</td>
<td> A | B = 3.</td>
</tr>
<tr>
<td>^</td>  <td>称为按位异或运算符。它对整型参数的每一个二进制位进行布尔异或操作。异或运算是指第一个参数或者第二个参数为true，并且不包括两个参数都为true的情况，则结果为true。</td>
<td>    (A ^ B) = 1.</td>
</tr>
<tr>
<td>~</td>  <td>称为按位非运算符。它是一个单运算符，对运算数的所有二进制位进行取反操作。</td>
<td>   ~B = -4 .</td>
</tr>
<tr>
<td>&lt;&lt;  </td>
<td>称为按位左移运算符。它把第一个运算数的所有二进制位向左移动第二个运算数指定的位数，而新的二进制位补0。将一个数向左移动一个二进制位相当于将该数乘以2，向左移动两个二进制位相当于将该数乘以4，以此类推。</td>    <td>A &lt;&lt; 1 = 4.</td>
</tr>
<tr>
<td>&gt;&gt;</td>
<td> 称为按位右移运算符。它把第一个运算数的所有二进制位向右移动第二个运算数指定的位数。为了保持运算结果的符号不变，左边二进制位补0或1取决于原参数的符号位。如果第一个运算数是正的，运算结果最高位补0；如果第一个运算数是负的，运算结果最高位补1。将一个数向右移动一位相当于将该数乘以2，向右移动两位相当于将该数乘以4，以此类推。</td>    <td>A &gt;&gt; 1 = 1.</td>
</tr>
<tr>
<td>&gt;&gt;&gt; </td>
<td>称为0补最高位无符号右移运算符。这个运算符与&gt;&gt;运算符相像，除了位移后左边总是补0.   </td>
<td>A &gt;&gt;&gt; = 1.</td> </tr> 
</tbody>
</table>   
 
## 赋值运算符 

JavaScript语言支持以下赋值运算符

<table>
<tbody>
<tr>
<th>运算符</th>  <th>描述</th>
<th> 例子</th>
</tr>
<tr>
<td>=   </td>
<td>简单赋值运算符，将右边运算数的值赋给左边运算数</td> <td>C = A + B 将A+B的值赋给C</td>
</tr>
<tr>
<td>+=  </td>
<td>加等赋值运算符，将右边运算符与左边运算符相加并将运算结果赋给左边运算数</td>
<td> C += A 相当于 C = C + A</td>
</tr>
<tr>
<td>-=  </td>
<td>减等赋值运算符，将左边运算数减去右边运算数并将运算结果赋给左边运算数 </td>
<td>C -= A 相当于C = C - A</td>
</tr>
<tr>
<td>*=  </td>
<td>乘等赋值运算符，将右边运算数乘以左边运算数并将运算结果赋给左边运算数</td>
<td>    C *= A 相当于C = C * A</td>
</tr>
<tr>
<td>/=  </td> <td>除等赋值运算符， 将左边运算数除以右边运算数并将运算结果赋值给左边运算数</td>
<td>   C /= A 相当于 C = C / A</td>
</tr>
<tr>
<td>%=  </td>
<td>模等赋值运算符，用两个运算数做取模运算并将运算结果赋值给左边运算数    </td>
<td>C %= A 相当于 C = C % A </td>
</tr>
</tbody>
</table>



## 其他运算符 

### 条件运算符

有一种运算符叫条件运算符。首先判断一个表达式是真或假，然后根据判断结果执行两个给定指令中的一个。条件运算符语法如下  

<table>
<tbody>
<tr>
<th>运算符</th>  <th>描述  </th>
<th>例子</th>
</tr>
<tr>
<td>? : </td>
<td>条件表达式</td>
<td>   如果条件为真 ? X值 : Y值 </td> </tr>
</tbody>
</table>

### typeof 运算符

typeof 是一个置于单个参数之前的一元运算符，这个参数可以是任何类型的。它的值是一个表示运算数的类型的字符串。  

typeof 运算符可以判断“数值”，“字符串”，“布尔”类型，看运算数是一个数字，字符串还是布尔值，并且根据判断结果返回true或者false。  

## if 语句 

**if**语句是基本的控制语句，能使JavaScript做出决定并且按条件执行语句。

```
    if (expression){
       Statement(s) to be executed if expression is true
    }
```

## if...else 语句 

**if...else** 语句是另一种控制语句，它能使JavaScript选择多个代码块之一来执行。  

```
    if (expression){
       Statement(s) to be executed if expression is true
    }else{
       Statement(s) to be executed if expression is false
    }
```

## if...else if... 语句 
**if...else if...** 语句是一种推进形式的控制语句，它能使 JavaScript 选择多个代码块之一来执行。  
  
  ```
     if (expression 1){
       Statement(s) to be executed if expression 1 is true
    }else if (expression 2){
       Statement(s) to be executed if expression 2 is true
    }else if (expression 3){
       Statement(s) to be executed if expression 3 is true
    }else{
       Statement(s) to be executed if no expression is true
    }
```

## switch-case 语句

语句的基本语法是给定一个判断表达式以及若干不同语句，根据表达式的值来执行这些语句。编译器检查每个**case**是否与表达式的值相匹配。如果没有与值相匹配的，则执行**default**缺省条件。  

```
    switch (expression)
    {
      case condition 1: statement(s)
    break;
      case condition 2: statement(s)
    break;
       ...
      case condition n: statement(s)
    break;
      default: statement(s)
    }  
```

## while 循环 



循环是 **JavaScript** 中最基本的循环模式，下边将加以介绍。  

```
    while(expression){  
    statement  
    }  
```

## do-while 循环语句

**do...while** 循环和 **while** 循环非常相似，它们之间的区别是 **while** 语句为先判断条件是否成立在执行循环体，而 **do...while** 循环语句则先执行一次循环后，再判断条件是否成立。也就是说即使判断条件不成立，**do...while** 循环语句中“{}”中的程序段至少要被执行一次。  

```
    do{  
    statement  
    }while(expression);  
```

## for 循环 

循环是一种最简洁的循环模式，包括三个重要部分  
- initialize ：初始化表达式,初始化计数器一个初始值，在循环开始前计算初始状态。
- test condition ：判断条件表达式，判断给定的状态是否为真。如果条件为真，则执行循环体“{}”中的代码，否则跳出循环。
- iteration statement ：循环操作表达式，改变循环条件，修改计数器的值。

可以将这三个部分放在同一行，用分号隔开。

```
    for(initialize;test condition;iteration statement)  
    {  
        statement;  
    }
```

## for in 语句 

```
    for (variablename in object){  
        statement
    }    
```

在每次迭代中将一个对象的属性赋值给变量，这个循环会持续到这个对象的所有属性都枚举完。  

## break 语句 

Break语句用于提前跳出循环,打破封闭的循环体。

## continue 语句 

Continue语句告诉解释器立即开始下一次迭代的循环和跳过剩余的代码块。  

当遇到continue语句,程序流将立即循环检查表达式,如果条件保持真那么下个迭代开始，否则控制跳出循环体。

## 函数定义 

使用一个函数之前,我们需要定义该函数。在 <em>JavaScript</em> 中最常见的定义一个函数的方式是使用函数关键字,紧随其后的是一个独特的函数名,参数列表(也可能是空的),和一个被花括号包围的语句块。这里显示的基本语法  

```
    <script type="text/javascript">
    <!--
    function functionname(parameter-list)
    {
      statements
    }
    //-->
    </script>
```

## 调用函数 

在脚本中调用某个函数之后,你会需要简单的编写的函数的名称如下

```
    <script type="text/javascript">
    
    <!--
    sayHello();
    //-->
    </script>
```

## 异常处理 

异常通常使用 *try/catch/finally* 结构来进行处理。  

```
    <script type="text/javascript">
    <!--
    try {
       statementsToTry
    } catch ( e ) {
      catchStatements
    } finally {
      finallyStatements
    }
    //-->
    </script>
```

try部分后面必须紧随catch后者finally部分（同时或者其一）。当在catch部分中发生异常事件后，异常会被存储于e变量中，然后catch部分会被执行。而finally部分会在try/catch之后必然执行。

## 警告对话框 

警告对话框是最常用的，它通常被用来给用户提示一些警告信息。比如，某个输入区域需要用户输入一些文本信息，但是用户并没有输入任何信息，那么为了使用户输入有效的信息，你可以利用警告对话框来提示警告信息，如下：

```
    <head>
    <script type="text/javascript">
    <!--
       alert("Warning Message");
    //-->
    
    </script>
    </head>
```

## 确认对话框 

确认对话框是最常用来获取用户对任何选项的赞成的观点。确认对话框会显示两个按钮：**Ok** 和 **Cancel**。  
你可以像如下的方式使用确认对话框：  

```
    <head>
    <script type="text/javascript">
    <!--
       var retVal = confirm("Do you want to continue ?");
       if( retVal == true ){
      alert("User wants to continue!");
    	  return true;
       }else{
      alert("User does not want to continue!");
    	  return false;
       }
    //-->
    </script>
    </head>
```

## 提示对话框 

你可以使用如下的方式来实现提示对话框 

```
    <head>
    <script type="text/javascript">
    <!--
       var retVal = prompt("Enter your name : ", "your name here");
       alert("You have entered : " +  retVal );
    //-->
    </script>
    </head>
```

## 页面重定向 

利用 JavaScript 在客户端进行重定向是非常简单的。为了重定向你的网站，你仅仅只需要在网页代码的头部中添加一行代码，如下  

```
    <head>
    <script type="text/javascript">
    <!--
       var retVal = prompt("Enter your name : ", "your name here");
       alert("You have entered : " +  retVal );
    //-->
    </script>
    </head>
```

## Void关键字 

JavaScript 中 void 是一个重要的关键字。它可以用作一个一元运算符，此时它会出现在一个操作数之前，这个操作数可以是任意类型的。   
这个操作符指定要计算一个表达式但是不返回值。它的语法可能是下列之一

```
    <head>
    <script type="text/javascript">
    <!--
    void func()
    javascript:void func()
    
    or:
    
    void(func())
    javascript:void(func())
    //-->
    </script>
    </head>
```

## 页面打印 

JavaScript 能使用 window 对象的打印函数**print**来帮你实现这个功能。

当JavaScript的打印方法 **window.print()** 执行后，就会打印当前的 web 页面。

你可以使用 onclick 事件直接调用这个函数，如下所示

```
    <head>
    <script type="text/javascript">
    <!--
    //-->
    </script>
    </head>
    <body>
    <form>
    <input type="button" value="Print" onclick="window.print()" />
    </form>
    </body>
```

## Cookies 的存储 

创建 Cookie 最简单的方式就是给 document.cookie 对象赋值一个字符串值，它的语法如下 

```
    document.cookie = "key1=value;key2=value2;expires=date";
```

## Cookies的读取 

读取 Cookie 就像写它一样简单，因为 *document.cookie* 对象的值就是 Cookie 的属性值。因此你可以利用这个字符串在任何时候对 Cookie 进行访问。  

*document.cookie* 字符串会保存一系列用分号分开的 name = value 键值对，这里的 name 就是一个 Cookie 名称，value 是它的值。
