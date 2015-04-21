# 循环控制

*JavaScript* 提供您完全控制来处理你的 *loops* 循环体和 *switch* 语句。可能会有这样一种情形，你需要在还没有到达循环体底部的时候跳出 *loop* 循环体。也可能存在这样的情况,当你想跳过一个代码块的一部分,想要开始下一个迭代。 
 
为处理所有这些情况, *JavaScript* 提供了 *break* 和 *continue*语句。这些语句用于立即跳出来任何循环或开始下一个迭代循环。 
 
## *Break* 语句  

Break语句,简要介绍了switch语句,用于早期退出循环,打破封闭的花括号。 
 
### 举例

这个例子演示了在一个while循环体内使用break语句。注意是怎样在x 等于5之前跳出循环体到达大括号下面的. write(. .)语句。  

``` 
    <script type="text/javascript">
    <!--
    var x = 1;
    document.write("Entering the loop<br /> ");
    while (x < 20)
    {
    if (x == 5){ 
    break;  // breaks out of loop completely
      }
      x = x + 1;
    document.write( x + "<br />");
    }
    document.write("Exiting the loop!<br /> ");
    //-->
    </script>  
```

产生的结果如下：  

```
    Entering the loop
    2
    3
    4
    5
    Exiting the loop!  
```
 
我们已经见过在switch语句里面使用break语句。  

## *Continue* 语句

Continue语句告诉解释器立即开始下一次迭代的循环和跳过剩余的代码块。

当遇到continue语句,程序流将立即循环检查表达式,如果条件保持真那么下个迭代开始，否则控制跳出循环体。  

### 举例

这个例子展示了 *continue* 语句在 *while* 循环语句的使用。当变量x达到5时， *continue* 语句用于跳过 *print* 语句。  

```
    <script type="text/javascript">
    <!--
    var x = 1;
    document.write("Entering the loop<br /> ");
    while (x < 10)
    {
      x = x + 1;
    if (x == 5){ 
    continue;  // skill rest of the loop body
      }
    document.write( x + "<br />");
    }
    document.write("Exiting the loop!<br /> ");
    //-->
    </script>
```

产生结果如下：  

```
    Entering the loop
    2
    3
    4
    6
    7
    8
    9
    10
    Exiting the loop!
```

## 使用标签来控制流
  
从 *JavaScript 1.2* ,开始，一个标签可以被用于 *break* , *continue* 语句去更精确地控制流。  
  
一个标签仅仅是一个标识符后跟一个冒号,应用于声明或代码块。我们将看到两个不同的例子来理解标签 *break* 和 *continue* 。 
 
注意:  *continue* 或 *break* 语句及其标签的名字之间不允许有换行符。当然标签名称和其后的的循环体之间也不应当有任何其他语句。  

### 例 1

```
    <script type="text/javascript">
    <!--
    document.write("Entering the loop!<br /> ");
    outerloop:   // This is the label name
    for (vari = 0; i< 5; i++)
    {
    document.write("Outerloop: " + i + "<br />");
    innerloop:
    for (var j = 0; j < 5; j++)
    {
    if (j >  3 ) break ; // Quit the innermost loop
    if (i == 2) break innerloop; // Do the same thing
    if (i == 4) break outerloop; // Quit the outer loop
    document.write("Innerloop: " + j + "  <br />");
       }
    }
    document.write("Exiting the loop!<br /> ");
    //-->
    </script>
```

将会产生如下的结果：  

```
    Entering the loop!
    Outerloop: 0
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    Innerloop: 3 
    Outerloop: 1
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    Innerloop: 3 
    Outerloop: 2
    Outerloop: 3
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    Innerloop: 3 
    Outerloop: 4
    Exiting the loop!
```

### 例 2


```
    <script type="text/javascript">
    <!--
    document.write("Entering the loop!<br /> ");
    outerloop:   // This is the label name
    for (vari = 0; i< 3; i++)
    {
    document.write("Outerloop: " + i + "<br />");
    for (var j = 0; j < 5; j++)
       {
    if (j == 3){
    continueouterloop;
      }
    document.write("Innerloop: " + j + "<br />");
       } 
    }
    document.write("Exiting the loop!<br /> ");
    //-->
    </script>
```

结果如下：  

```
    Entering the loop!
    Outerloop: 0
    Innerloop: 0
    Innerloop: 1
    Innerloop: 2
    Outerloop: 1
    Innerloop: 0
    Innerloop: 1
    Innerloop: 2
    Outerloop: 2
    Innerloop: 0
    Innerloop: 1
    Innerloop: 2
    Exiting the loop!
```
