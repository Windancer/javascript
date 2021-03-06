# 对象概述

JavaScript 是一种面向对象编程语言 ( OOP ) 。一种语言如果可以为开发者提供四种基本功能就可以被称为面向对象:  

- **封装**：把相关信息，无论数据或方法都存储在一个对象中的能力。  
- **聚合**：将一个对象存储在另一个对象中的能力。  
- **继承**：一个类依赖另一个类 （ 或一些类 ）中的一些性质和方法的能力。  
- **多态**：写一个函数或方法，这个函数或方法可以以各种不同形式工作的能力。  

对象由属性组成。如果一个属性包含一个函数，它被认为是这个对象的一个方法，否则这个属性被认为成一个属性。 

## 对象的属性

对象属性可以是任何三个基本数据类型，或抽象数据类型中的任何一个，如另一个对象。对象属性通常是在对象的方法内部使用的变量，也可以是在整个页面中使用的全局变量。  
 
将属性添加到对象的语法是：
 
``` 
objectName.objectProperty = propertyValue； 
```

### 示例

以下是一个简单的例子，介绍了如何使用文档对象的 “title” 属性来获得一个文档标题:  

```      
var str = document.title;
```

## 对象的方法

方法是函数让对象做某事或让某事作用在这个对象上。一个函数和一个方法之间，除了函数是声明的一个独立的单元，而方法是附加到某个对象上并且可以使用 `this` 关键字引用方法，除此之外几乎没有差别。 
 
方法从将对象的内容显示到屏幕上到对一组本地属性和参数执行复杂的数学运算都很有用。  

### 示例
  
以下是一个简单的例子，介绍了怎样使用文档对象的 **write()** 方法在文档中写任何内容:   

```
document.write("This is test");
```

## 用户定义的对象

所有用户定义的对象和对象中的内置对象都是一个被称为 Object 的对象的后代。 
 
### new 运算符

new 运算符用于创建对象的实例。若要创建一个对象，new 运算符后紧接着是构造函数方法。    

在以下示例中，构造函数方法是 Object() ， Array() ，和 Date() 。这些函数是内置的 JavaScript 函数。

```  
var employee = new Object();  
var books = new Array("C++","Perl","Java");  
var day = new Date("August 15,1947");   
```

### Object() 构造函数

构造函数是一个可以创建和初始化对象的函数。 JavaScript 提供了名为  Object() 的一个特殊的构造函数来生成对象。 Object() 构造函数将返回值赋给一个变量。  

### 示例 1

此示例演示如何创建一个对象：

```
    <html>
    <head>
    <title>User-defined objects</title>
    <script type="text/javascript">
    var book = new Object();   // Create the object
        book.subject = "Perl"; // Assign properties to the object
        book.author  = "Mohtashim";
    </script>
    </head>
    <body>
    <script type="text/javascript">
       document.write("Book name is : " + book.subject + "<br>");
       document.write("Book author is : " + book.author + "<br>");
    </script>
    </body>
    </html>
```    

### 示例 2

此示例演示了如何用用户定义的函数来创建一个对象。这里的 this 关键字用于引用被传递给函数的对象。  
 
``` 
    <html>
    <head>
    <title>User-defined objects</title>
    <script type="text/javascript">
    function book(title, author){
        this.title = title; 
        this.author  = author;
    }
    </script>
    </head>
    <body>
    <script type="text/javascript">
       var myBook = new book("Perl", "Mohtashim");
       document.write("Book title is : " + myBook.title + "<br>");
       document.write("Book author is : " + myBook.author + "<br>");
    </script>
    </body>
    </html>
```    

## 为对象定义的方法

前面的示例演示了如何用构造函数创建对象和分配属性。但是我们需要通过给对象分配方法来完成一个对象的定义。  

### 示例

这里是一个简单的示例，说明了如何与一个对象一起添加一个函数。  

```
    <html>
    <head>
    <title>User-defined objects</title>
    <script type="text/javascript">
    
    // Define a function which will work as a method
    function addPrice(amount){
        this.price = amount; 
    }
    
    function book(title, author){
        this.title = title; 
        this.author  = author;
        this.addPrice = addPrice; // Assign that method as property.
    }
    
    </script>
    </head>
    <body>
    <script type="text/javascript">
       var myBook = new book("Perl", "Mohtashim");
       myBook.addPrice(100);
       document.write("Book title is : " + myBook.title + "<br>");
       document.write("Book author is : " + myBook.author + "<br>");
       document.write("Book price is : " + myBook.price + "<br>");
    </script>
    </body>
    </html>
```  

## with 关键字

with 关键字被用来作为用于引用一个对象的属性或方法的一种速记。  

对象被指定成 with 关键字的参数，进而成为后面语句块的默认对象。这个对象的下的属性和方法可以不指定对象名而直接使用。 
### 语法  

```
     with (object){
    properties used without the object name and dot
    }    
```

### 示例

``` 
    <html>
    <head>
    <title>User-defined objects</title>
    <script type="text/javascript">
    
    // Define a function which will work as a method
    function addPrice(amount){
    with(this){
       price = amount; 
    }
    }
    function book(title, author){
        this.title = title; 
        this.author  = author;
        this.price = 0;
        this.addPrice = addPrice; // Assign that method as property.
    }
    </script>
    </head>
    <body>
    <script type="text/javascript">
       var myBook = new book("Perl", "Mohtashim");
       myBook.addPrice(100);
       document.write("Book title is : " + myBook.title + "<br>");
       document.write("Book author is : " + myBook.author + "<br>");
       document.write("Book price is : " + myBook.price + "<br>");
    </script>
    </body>
    </html>    
```

## JavaScript Native 对象

JavaScript 有几个内置或 native 对象。这些对象可以在任何地方被访问，并且在任何浏览器中运行的任何操作系统的工作方式相同。  

这里是所有重要的 JavaScript native 对象的列表：  

- [JavaScript Number Object](number.md)  

- [JavaScript Boolean Object](boolean.md)  

- [JavaScript String Object](string.md)  

- [JavaScript Array Object](array.md)  

- [JavaScript Date Object](date.md)  

- [JavaScript Math Object](math.md)  

- [JavaScript RegExp Object](regexp.md)  























