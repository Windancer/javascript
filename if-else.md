通常在写代码时，您总是需要为不同的决定来执行不同的动作。因此你需要利用条件语句来使你的程序做出正确决定并且执行正确的动作。

JavaScript支持的条件语句用于基于不同的条件来执行不同的动作。下面我们看一下**if...else**语句。

JavaScript支持如下形式的**if...else**语句：

- if statement

- if...else statement

- if...else if... statement.  

##if语句：

**if**语句是基本的控制语句，能使JavaScript做出决定并且按条件执行语句。

##语法：
    if (expression){
       Statement(s) to be executed if expression is true
    }

这里JavaScript *expression*是需要判断的。如果返回值是*true*，执行给定的 *statement(s)*。如果表达式的值是*false* ，不会执行任何语句。多数情况下，你可能会用比较运算符来做决定。

##例子：
    <script type="text/javascript">
    <!--
    var age = 20;
    if( age > 18 ){
       document.write("<b>Qualifies for driving</b>");
    }
    //-->
    </script>
程序运行结果如下：
    
    Qualifies for driving

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_32)


##if...else 语句:
**if...else** 语句是另一种控制语句，它能使JavaScript选择多个代码块之一来执行。

##语法：
    if (expression){
       Statement(s) to be executed if expression is true
    }else{
       Statement(s) to be executed if expression is false
    }

这里JavaScript *expression*是需要判断的。如果返回值是*true*，执行if代码块给定的*statement(s)*。如果表达式的值是*false* ，则执行else代码块给定的*statement(s)*。

##例子：
    <script type="text/javascript">
    <!--
    var age = 15;
    if( age > 18 ){
       document.write("<b>Qualifies for driving</b>");
    }else{
       document.write("<b>Does not qualify for driving</b>");
    }
    //-->
    </script>

程序运行结果如下：

    Does not qualify for driving

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_32)

##if...else if...语句：
**if...else if...** 语句是一种推进形式的控制语句，它能使JavaScript选择多个代码块之一来执行。
##语法：
    if (expression 1){
       Statement(s) to be executed if expression 1 is true
    }else if (expression 2){
       Statement(s) to be executed if expression 2 is true
    }else if (expression 3){
       Statement(s) to be executed if expression 3 is true
    }else{
       Statement(s) to be executed if no expression is true
    }
这段代码没什么特别的地方。它就是一系列 *if* 语句，只是每个 *if* 语句是前一个 *else* 语句的一部分。语句根据正确的条件被执行，如果不满足任何一个条件则执行 *else* 代码块。
##例子：
    <script type="text/javascript">
    <!--
    var book = "maths";
    if( book == "history" ){
       document.write("<b>History Book</b>");
    }else if( book == "maths" ){
       document.write("<b>Maths Book</b>");
    }else if( book == "economics" ){
       document.write("<b>Economics Book</b>");
    }else{
      document.write("<b>Unknown Book</b>");
    }
    //-->
    </script>
程序运行结果如下：

    Maths Book

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_32)


