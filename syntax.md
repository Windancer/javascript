# 语法

一个 JavaScript 包括那些在 HTML 中放置在 `<script> ... </script>` 标签内的 JavaScript 语句。

你可以把包含你的 JavaScript 的 `<script>` 标签放置在你的网页的任何地方，但是保存在 `<head>` 标签内是它的首选方式。

`<script>` 标签作为一个脚本，提醒浏览器程序开始解释在这些标签之间的所有的文本。所以你的 JavaScript 的简单语法将会像下列一样。

```
    <script ...>
        JavaScript 代码
    </script>
```

脚本标签有两个重要属性:

- **语言**：该属性制定你使用的脚本语言。通常情况下，它的值将会是 *javascript*。尽管最近的 HTML 版本（ 包括 XHTML，它的继任者 ）不再使用这个属性。

- **类型**：该属性是现在被推荐来指示所使用的脚本语言，它的值应被设置为 ” *text*/*javascript* ”。

所以你的 JavaScript 的片段应该是像这样：

```
    <script language="javascript" type="text/javascript">
        JavaScript 代码
    </script>
```

## 你的第一个 JavaScript 脚本

让我们来写出课上的例子来打印出 “ Hello World ”。

```
    <html>
    <body>
    <script language="javascript" type="text/javascript">
    <!--
       document.write("Hello World!")
    //-->
    </script>
    </body>
    </html>
```

我们增加了一个可选的 HTML 注释，围绕着我们的 JavaScript 代码。这是为了在一个不支持 JavaScript 的浏览器中节省我们的代码。注释以 ”//-->” 结尾。这里 ”//” 标志着 JavaScript 中的注释，所以我们增加它来阻止一个浏览器把 HTML 的注释的结尾作为 JavaScript 代码的一部分来阅读。

另外，我们调用一个函数 *ducument.write*,它将一个字符串写进我们的 HTML 文档。这个函数可以被用来书写正文、HTML 或者两个一起。所以上面的代码会显示下面的结果。

```
    Hello World!
```

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_1)。

## 空格和换行

JavaScript 忽略出现在 JavaScript 中的空格，制表符和换行符。

因为你可以在你的程序中自由的使用空格，制表符，换行符，所以你可以自由的用一个整洁的，一致的方法格式化和缩进你的程序，来使得代码易于阅读和理解。

## 分号是可选的

在 JavaScript 中简单语句通常后面跟着一个分号，正如 C,C++ 和Java 中一样。然而，JavaScript 允许你忽略这个分号，如果你的每个陈述都放在一个单独的行。例如，下面的代码就可以不写分号。

```
    <script language="javascript" type="text/javascript">
    <!--
      var1 = 10
      var2 = 20
    //-->
    </script>
```

但是，当像下面这样书写一行时，就需要分号了。

```
    <script language="javascript" type="text/javascript">
    <!--
      var1 = 10; var2 = 20;
    //-->
    </script>
```

**注意**：使用分号是一个非常好的编程习惯。

## 区分大小写

JavaScript 是一种区分大小写的语言。这意味着语言的关键字，变量，函数名，以及任何其他的标识符必须使用一致的大小写字母类型。

所以标识符 *Time*，*TIme* 和 *TIME* 在 JavaScript 中有不同的含义。

**注意：**当你在 JavaScript 中写变量和函数名中应该特别注意。

## JavaScript中的注释

JavaScript 支持 C 形式和 C++ 形式的注释，即：

- 在 // 之间的任何文本和最后一行都被视为是注释，都被 JavaScript 所忽略。

- 在字母 /* 和 */ 之间的任何文本都被视为注释。它可以是多行。

- JavaScript 还可以识别 HTML 注释的开始语句 <!--.JavaScript 把它视为一个当行注释，就像 // 注释一样处理。

- JavaScript 不能识别 HTML 注释的结束语句 -->，所以可以写成 //-->。

## 例子

```
    <script language="javascript" type="text/javascript">
    <!--
    // This is a comment. It is similar to comments in C++
    /*
     * This is a multiline comment in JavaScript
     * It is very similar to comments in C Programming
     */
    //-->  
    </script>
```