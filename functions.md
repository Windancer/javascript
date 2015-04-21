# 函数

函数是一组可重用的代码，你可以在你程序的任何地方调用他。这使你不需要一遍又一遍地写相同的代码。这将帮助程序员编写模块代码。你可以把大项目在许多小和易于管理的功能。你可以把你的大型程序分成许多的小型的且易于管理的函数。

像任何其他高级编程语言，*JavaScript* 还支持使用函数编写模块代码所需的所有特性。  

你一定在之前的章节见过 *alert()* 和 *write()* 函数。虽然我们将一次又一次的使用这些函数，但是他们已经被一次性的写在核心 *JavaScript* 。  

*JavaScript* 使我们能够编写自己的函数。这一节将解释如何用 *JavaScript* 编写自己的函数。

## 函数定义

我们使用一个函数之前,我们需要定义该函数。在 *JavaScript* 中最常见的定义一个函数的方式是使用函数关键字,紧随其后的是一个独特的函数名,参数列表(也可能是空的),和一个被花括号包围的语句块。这里显示的基本语法:  

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

### 例子

一个不需要参数的简单的函数定义如下：  

```
    <script type="text/javascript">
    <!--
    function sayHello()
    {
        alert("Hello there");
    }
    //-->
    </script>
```
    
### 调用函数

在脚本中调用某个函数之后,你会需要简单的编写的函数的名称如下: 

```
    <script type="text/javascript">
    <!--
    sayHello();
    //-->
    </script>
```
    
## 函数参数

到目前为止，我们已经看到了没有参数的函数，但这些函数里面都有一个功能就是去传递不同的参数。这些被传递的参数可以在函数内被捕获且可以在这些函数上进行任何操作。在一个函数内可以把多个参数用逗号隔开。

### 例子

让我们在sayhello函数上做一些修改。这次会有两个参数。  

```
    <script type="text/javascript">
    <!--
    function sayHello(name, age)
    {
       alert( name + " is " + age + " years old.");
    }
    //-->
    </script>
```
    
**注意:** 我们使用+运算符连接字符串和数字。*JavaScript* 不介意将数字添加到字符串里。  

现在，我们可以调用如下这个函数:  

```    
    <script type="text/javascript">
    <!--
    sayHello('Zara', 7 );
    //-->
    </script>
```

### reture 语句

一个 *JavaScript* 函数可以有一个可选的返回语句。这是必需的,如果你想从一个函数返回一个值。这个语句应该是函数里的最后一个语句。  

例如你可以在一个函数内输入两个数字,然后你可以从函数返回调用他们相乘的结果。  

### 例子

这个函数把两个参数连接起来并在调用程序中奖结果返回：  

```    
    <script type="text/javascript">
    <!--
    function concatenate(first, last)
    {
       var full;
    
       full = first + last;
       return  full;
    }
    //-->
    </script>
```
    
现在我们可以像下面这样调用这个函数：  

```
    <script type="text/javascript">
    <!--
       var result;
       result = concatenate('Zara', 'Ali');
       alert(result );
    //-->
    </script>
```
   
## 函数的高级概念

关于JavaScript函数我们已经了解了很多，但是我也在本教程放置了如下的重要概念。如果你有时间我会建议你至少去去浏览一下它们。

- [JavaScript Nested Functions](http://www.tutorialspoint.com/javascript/javascript_nested_functions.htm)
- [JavaScript Function( ) Constructor](http://www.tutorialspoint.com/javascript/javascript_function_constructors.htm)
- [JavaScript Function Literals](http://www.tutorialspoint.com/javascript/javascript_function_literals.ht)






