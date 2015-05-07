## 图像映射

您可以使用 JavaScript 来创建客户端的图像映射。 usemap 启用客户端图像映射的属性定义的 &lt;img /&gt; 标记和特殊的 &lt;map&gt; 和  &lt;area&gt; 扩展标签。  

一般情况下，用 &lt;map&gt; 将形成映射的图像插入到页面，此外它带有一个额外的属性称为 usemap 。usemap 属性的值是&lt;map&gt; element 上的 name 属性的值。   

&lt;map&gt; 元素实际上创建的地图图片，通常遵循后直接 &lt;img /&gt; 元素。它为&lt;area /&gt; element充当一个容器，&lt;area /&gt; element 用于定义可点击的热点。&lt;map&gt; element只有一个属性，即名称属性，用于标识映射。这就是为什么 &lt;img /&gt; 元素知道使用哪个 &lt;map&gt; element。  

&lt;area&gt; 元素指定坐标定义边界的形状和每一个可点击的热点。  

当鼠标移动到图像的不同部分时，以下结合 imagemap 和 JavaScript 在一个文本框里面产生一个消息。

```
    <html>
    <head>
    <title>Using JavaScript Image Map</title>
    <script type="text/javascript">
    <!--
    function showTutorial(name){
      document.myform.stage.value = name
    }
    //-->
    </script>
    </head>
    <body>
    <form name="myform">
       <input type="text" name="stage" size="20" />
    </form>
    <!-- Create  Mappings -->
    <img src="/images/usemap.gif" alt="HTML Map" 
    border="0" usemap="#tutorials"/>
    
    <map name="tutorials">
       <area shape="poly" 
    coords="74,0,113,29,98,72,52,72,38,27"
    href="/perl/index.htm" alt="Perl Tutorial"
    target="_self" 
    onMouseOver="showTutorial('perl')" 
    onMouseOut="showTutorial('')"/>
    
       <area shape="rect" 
    coords="22,83,126,125"
    href="/html/index.htm" alt="HTML Tutorial" 
    target="_self" 
    onMouseOver="showTutorial('html')" 
    onMouseOut="showTutorial('')"/>
    
       <area shape="circle" 
    coords="73,168,32"
    href="/php/index.htm" alt="PHP Tutorial"
    	target="_self" 
    onMouseOver="showTutorial('php')" 
    onMouseOut="showTutorial('')"/>
    </map>
    </body>
    </html>
   ```


