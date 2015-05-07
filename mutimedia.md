## 多媒体

JavaScript 导航对象包含的子对象称为插件。这个对象是一个数组，每个插件会在浏览器上安装一个条目。导航器和插件对象只被网景，Firefox 和 Mozilla 支持。

下面是一个示例，列出了所有安装浏览器上的插件:

```
    <html>
    <head>
    <title>List of Plug-Ins</title>
    </head>
    <body>
    <table border="1">
    <tr>
    <th>Plug-in Name</th>
    <th>Filename</th>
    <th>Description</th>
    </tr>
    <script language="JavaScript" type="text/javascript">
    for (i=0; i<navigator.plugins.length; i++) {
       document.write("<tr><td>");
       document.write(navigator.plugins[i].name);
       document.write("</td><td>");
       document.write(navigator.plugins[i].filename);
       document.write("</td><td>");
       document.write(navigator.plugins[i].description);
       document.write("</td></tr>");
    }
    </script>
    </table>
    </body>
    </html>
```

### 检查插件

每个插件在数组中都有一个入口。每个入口有以下属性：

- 名字——是插件的名称。
- 文件名——是加载安装插件的可执行文件。
- 描述——是对于插件的描述，由开发人员提供。
- mimetype——是有一个入口的数组，这个入口是被插件支持的 MIME 类型的入口。

您可以使用这些属性在脚本中找到已安装的插件，然后使用 JavaScript可以适当运行的多媒体文件如下：

```
    <html>
    <head>
    <title>Using Plug-Ins</title>
    </head>
    <body>
    <script language="JavaScript" type="text/javascript">
    media = navigator.mimeTypes["video/quicktime"];
    if (media){
      document.write("<embed src='quick.mov' height=100 width=100>");
    }
    else{
      document.write("<img src='quick.gif' height=100 width=100>");
    }
    </script>
    </body>
    </html>
```
    
**注意：**我们使用 HTML &lt;embed&gt; 标记中嵌入一个多媒体文件。

### 多媒体控制

让我们举一个真实的例子，它在几乎所有的浏览器里面都有效：

```
    <html>
    <head>
    <title>Using Embeded Object</title>
    <script type="text/javascript">
    <!--
    function play()
    {
    document.demo.Play();
      }
    }
    function stop()
    {
      if (document.demo.IsPlaying()){
    document.demo.StopPlay();
      }
    }
    function rewind()
    {
      if (document.demo.IsPlaying()){
    document.demo.StopPlay();
      }
      document.demo.Rewind();
    }
    //-->
    </script>
    </head>
    <body>
    <embed id="demo" name="demo"
    src="http://www.amrood.com/games/kumite.swf"
    width="318" height="300" play="false" loop="false"
    pluginspage="http://www.macromedia.com/go/getflashplayer"
    swliveconnect="true">
    </embed>
    <form name="form" id="form" action="#" method="get">
    <input type="button" value="Start" onclick="play();" />
    <input type="button" value="Stop" onclick="stop();" />
    <input type="button" value="Rewind" onclick="rewind();" />
    </form>
    </body>
    </html>
```

