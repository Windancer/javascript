## Javascript——浏览器兼容性

重要的是要了解不同浏览器之间的差异，以处理每个预计会出现的问题。所以重要的是要知道哪个浏览器运行在您的 Web 页面。   

获得目前运行在 Web 页面的浏览器的信息，使用内置的 **navigator** 对象。

### 导航属性：
有几个导航相关属性，您可以使用您的 Web 页面。下面是一个列表的名称和描述：
<table>
<tr>
<th>属性</th>
<th>描述</th>
</tr>
<tr>
<td>appCodeName</td>
<td> 这个属性是一个包含浏览器 code name 的字符串，比如 Netscape 是 Netscape 的 code name ， Microsoft Internet Explorer 是 Internet Explorer 的code name。</td>
</tr>
<tr>
<td>Appversion</td>
<td>这个属性是一个字符串，其中包含浏览器的版本以及其他有用的信息，比如它的语言和兼容性。</td>
</tr>
<tr>
<td>language</td>
<td>这个属性包含两个字母的缩写表示这种语言，使用这种方式的浏览器只有 Netscape。</td>
</tr>
<tr>
<td>mimTypes[]</td>
<td>这个属性是一个数组，其中包含所有客户端支持的 MIME 类型。只有 Netscape。</td>
</tr>
<tr>
<td>platform[] </td>
<td>这个属性是一个字符串，其中包含浏览器编译的平台。“Win32”32 位 Windows 操作系统。</td>
</tr>
<tr>
<td>plugins[]</td>
<td>这个属性是一个数组，其中包含的所有插件已经安装在客户机上。只有 Netscape 公司。</td>
</tr>
<tr>
<td>userAgent[]</td>
<td> 这个属性是一个字符串，其中包含浏览器的代码名称和浏览器版本。这个值被发送到原始服务器用于识别客户端。</td>
</tr>
</table>
### 导航方法:
有几个 Navigator-specific 方法。这里是一个与其相关的列表的：
<table>
<tr>
<th>方法</th>
<th>描述</th>
</tr>
<tr>
<td>javaEnabled()</td>
<td>这个方法确定是否启用了 JavaScript 客户端。如果启用了 JavaScript，那么该方法将返回 true，否则返回 false。</td>
</tr>
<tr>
<td>plugings.refresh</td>
<td>这个方法使新安装的插件可用，并且用所有新插件的名称去填充插件数组。 Netscape 公司 only。</td>
</tr>
<tr>
<td>preference(name,value)</td>
<td>这种方法允许标记脚本去获取和设置一些 Netscape 的偏好。如果省略第二个参数，那么该方法将返回的值指定的偏好；否则，使用系统默认的值。 Netscape 公司 only。</td>
</tr>
<tr>
<td>taintEnabled()</td>
<td>这个方法返回 true，如果启用了数据污染，否则，则返回 false。</td>
</tr>
</table>
### 浏览器检测:
有一个简单的 JavaScript 可以用来发现浏览器的名称 ,其后相应的 HTML 页面可以被提供给用户。

    <html>
    <head>
    <title>Browser Detection Example</title>
    </head>
    <body>
    <script type="text/javascript">
    <!--
    var userAgent   = navigator.userAgent;
    var opera   = (userAgent.indexOf('Opera') != -1);
    var ie  = (userAgent.indexOf('MSIE') != -1);
    var gecko   = (userAgent.indexOf('Gecko') != -1);
    var netscape= (userAgent.indexOf('Mozilla') != -1);
    var version = navigator.appVersion;
    
    if (opera){
      document.write("Opera based browser");
      // Keep your opera specific URL here.
    }else if (gecko){
      document.write("Mozilla based browser");
      // Keep your gecko specific URL here.
    }else if (ie){
      document.write("IE based browser");
      // Keep your IE specific URL here.
    }else if (netscape){
      document.write("Netscape based browser");
      // Keep your Netscape specific URL here.
    }else{
      document.write("Unknown browser");
    }
    // You can include version to along with any above condition.
    document.write("<br /> Browser version info : " + version );
    //-->
    </script>
    </body>
    </html>

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_49)。

