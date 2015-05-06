## 调试
当你写程序的时候很有可能出现错误，这在脚本中被称为一个bug。   

发现和修复 bug 的过程叫做调试，是一个正常的开发过程的一部分。本节讨论的工具和技术，可以帮助您进行任务调试。   

### IE 浏览器里面的错误信息
跟踪错误的最基本的方法是在您的浏览器中打开错误信息。默认情况下，当一个错误发生在页面，Internet Explorer 在状态栏显示错误图标：

![image1](images/error_icon.gif)

双击这个图标将您带到一个对话框，这个对话框将会显示发生的特定的错误信息。  

因为这个图标很容易忽视，当发生错误时，Internet Explorer 提供了选项自动显示错误对话框。   

要启用这个选项，选择 **Tools --> Internet Options --> Advanced tab**。最后通过检查显示一个关于每一个脚本错误框的通知，选项如下所示：

![image2](images/error_console.gif)

### 在 Mozilla 或 Firefox 里的错误消息
火狐 Netscape 和 Mozilla 等浏览器将错误消息发送到一个叫做 JavaScript 控制台或错误控制台的特殊窗口。查看控制台，选择 **Tools-->Error Consol or Web Development。**   

不幸的是，因为这些浏览器在一个错误发生时，没有给出视觉的标示，你必须保持打开控制台，才能看您的脚本执行的错误。

![image3](images/internet_options.gif)
### 错误通知
错误通知，出现在控制台或通过 IE 浏览器对话框里的错误是语法和运行时错误的结果。这些错误通知会显示错误所在的行号当错误发生时。  

如果您使用的是 Firefox浏览器，那么你可以点击在错误控制台脚本中可以获得的错误从而到达有错误的那一行。  
### 如何调试脚本
有多种方法来调试 JavaScript：
#### 用一个 JavaScript 验证器
检查您的 JavaScript 代码出现的奇怪的错误的一种方法是通过程序来运行它，检查它以确保它是有效的。这是官方语言的语法规则。这些程序被称为验证解析器，也可以简称为验证器，通常是存在于商业HTML和JavaScript编辑器。  

最方便的 JavaScript 验证器是 Douglas Crockford's JavaScript Lint，Douglas Crockford's JavaScript Lint 可以免费在线使用。   

简单地访问这个网页,将 JavaScript 代码(只有 JavaScript )粘贴到文本区域,并单击 jslint 按钮。这个程序将通过您的 JavaScript 代码解析,确保任何变量和函数定义遵循正确的语法。它还将检查 JavaScript 语句,比如 if 和 whil e语句,以确保他们也遵循正确的格式

#### 添加调试代码到您的程序
您可以在你的程序中使用 alert() 或 document . write() 方法去调试你的代码。例如,你应该这样写：

    var debugging = true;
    var whichImage = "widget";
    if( debugging )
       alert( "Calls swapImage() with argument: " + whichImage );
    var swapStatus = swapImage( whichImage );
    if( debugging )
       alert( "Exits swapImage() with swapStatus=" + swapStatus );

当他们出现的时候，通过检测程序内容和alert()s的命令，你可以非常容易的确定你的程序是否有错误。

#### 使用一个JavaScript调试器
调试器是一个应用程序，该应用程序确保各种各样的脚本在程序员的控制下执行。脚本调试器通过一个界面提供细粒度的控制的状态，允许您检查和设置值以及控制流执行。  

一旦一个脚本被加载到一个调试器，它可以每次运行一行或指示停止在某个断点。一旦停止执行，程序员可以检查脚本和它的状态变量，以确定是否有地方出了问题。你也可以观察变量的变化值。   

最新版本的 Mozilla JavaScript 调试器（代号为完 Venkman ）Mozilla 和 Netscape 浏览器可以下载
[http://www.hacksrus.com/~ginda/venkman](http://www.hacksrus.com/~ginda/venkman/)
#### 对开发人员有用的技巧
这里有几个技巧，您可以使用在你的脚本中用于减少错误的数量，同时使调试过程更容易一些。   

- 记住要使用大量的注释。注释使您能够解释为什么你以这样的方式书写脚本和解释特别困难的部分代码。
- 总是使用缩进，使代码易于阅读。缩进语句也使你更容易匹配开始和结束标记，花括号和其他 HTML 和脚本元素。
- 编写模块代码。只要有可能，用函数的形式来组织你的语句。函数使你能够阻止相关语句，并以最小的努力测试和重用的部分代码以。
- 命名变量和函数的方法要一致。尝试使用足够长的时间有意义的名称，描述的内容变量或函数的目的。
- 命名变量和函数时使用一致的语法。换句话说，让他们所有的小写或大写；如果你喜欢 Camel-Back 符号，一致地使用它。 
- 以模块化的方式测试长脚本。换句话说，不要试图在编写完成整个脚本之后再测试它的任何部分。写一段，使它能够工作之后，再添加代码的下一部分。
- 使用描述性的变量和函数名称和避免使用单个字符的名称。
- 注意你的引号。记住，引号用于对字符串和这两个引号必须相同的风格(单引号或双)。
- 主义你的等于号。你不应该一个 = 用于比较的目的。
- 声明变量显式地使用 var 关键字。
