# Switch Case

你可以像前面章节那样用多个 *if…else if* 语句来执行多个代码块。然而，这不是最佳解决方案，尤其是当所有代码块的执行依赖于单个变量值时。

从 JavaScript 1.2 开始，你可以使用一个 **switch** 语句来处理上面提到的问题，而且这样做的效率远高于重复使用if…else if 语句。

## 语法

**switch**语句的基本语法是给定一个判断表达式以及若干不同语句，根据表达式的值来执行这些语句。编译器检查每个**case**是否与表达式的值相匹配。如果没有与值相匹配的，则执行缺省条件。  

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
    
**break**语句用于在特殊case的最后终止程序。如果省略掉break，编译器将继续执行下面每个case里的语句。

我们将在循环控制那一章节里继续讨论**break**语句。
## 例子

下面这个例子演示了一个基本的while循环：

```
    <script type="text/javascript">
    <!--
    var grade='A';
    document.write("Entering switch block<br />");
    switch (grade)
    {
      case 'A': document.write("Good job<br />");
    break;
      case 'B': document.write("Pretty good<br />");
    break;
      case 'C': document.write("Passed<br />");
    break;
      case 'D': document.write("Not so good<br />");
    break;
      case 'F': document.write("Failed<br />");
    break;
      default:  document.write("Unknown grade<br />")
    }
    document.write("Exiting switch block");
    //-->
    </script>
```

程序运行结果如下：

```
    Entering switch block
    Good job
    Exiting switch block
```

## 例子

看一下如果没用**break**语句的情况：

```
    <script type="text/javascript">
    <!--
    var grade='A';
    document.write("Entering switch block<br />");
    switch (grade)
    {
      case 'A': document.write("Good job<br />");
      case 'B': document.write("Pretty good<br />");
      case 'C': document.write("Passed<br />");
      case 'D': document.write("Not so good<br />");
      case 'F': document.write("Failed<br />");
      default:  document.write("Unknown grade<br />")
    }
    document.write("Exiting switch block");
    //-->
    </script>
```

程序运行结果如下：

```
    Entering switch block
    Good job
    Pretty good
    Passed
    Not so good
    Failed
    Unknown grade
    Exiting switch block
```

