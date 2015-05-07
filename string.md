## 字符串对象

**String** 对象通过大量的辅助方法来操作一系列字符的组合（即字符串），这些方法隐藏了 JavaScript 字符串原始数据类型。

因为 JavaScript 可以实现原始字符串数组和字符串对象之间的自动转换，你可以调用字符串对象的任何一个辅助方法作用于原始字符串数据。
### 语法

创建一个 **String** 对象：
  
```   
var val = new String(string);
```

参数 string 是正确编码的字符序列。

### String属性

下边列出了 String 的各个属性及对应的属性描述。 

<table >
<tr>
<th align="left">属性</th>
<th align="left">描述</th>
</tr>
<tr>
<td>constructor</a></td>
<td>对创建该对象的函数的引用</td>
</tr>
<tr>
<td>length</a></td>
<td>字符串的长度</td>
</tr>
<tr>
<td>prototype</a></td>
<td>允许向对象添加属性和方法</td>
</tr>
</table>

### String对象方法

下边列出了 String 的一系列方法及对应的描述。

<table >
<tr>
<th align="left">方法</th>
<th align="left">描述</th>
</tr>
<tr>
<td>charAt()</a></td>
<td>返回在指定位置的字符</td>
</tr>
<tr>
<td>charCodeAt()</a></td>
<td>返回在指定的位置的字符的 Unicode 编码</td>
</tr>
<tr>
<td>concat()</a></td>
<td>连接字符串</td>
</tr>
<tr>
<td>indexOf()</a></td>
<td>检索字符串</td>
</tr>
<tr>
<td>lastIndexOf()</a></td>
<td>从后向前检索字符串</td>
</tr>
<tr>
<td>localeCompare()</a></td>
<td>用本地特定的顺序来比较两个字符串</td>
</tr>
<tr>
<td>match()</a></td>
<td>找到一个或多个正则表达式的匹配</td>
</tr>
<tr>
<td>replace()</a></td>
<td>替换与正则表达式匹配的子串</td>
</tr>
<tr>
<td>search()</a></td>
<td>检索与正则表达式相匹配的值</td>
</tr>
<tr>
<td>slice()</a></td>
<td>提取字符串的片断，并在新的字符串中返回被提取的部分</td>
</tr>
<tr>
<td>split()</a></td>
<td>把字符串分割为字符串数组</td>
</tr>
<tr>
<td>substr()</a></td>
<td>从起始索引号提取字符串中指定数目的字符</td>
</tr>
<tr>
<td>substring()</a></td>
<td>提取字符串中两个指定的索引号之间的字符</td>
</tr>
<tr>
<td>toLocaleLowerCase()</a></td>
<td>把字符串转换为小写</td>
</tr>
<tr>
<td>toLocaleUpperCase()</a></td>
<td>把字符串转换为大写</td>
</tr>
<tr>
<td>toLowerCase()</a></td>
<td>把字符串转换为小写</td>
</tr>
<tr>
<td>toString()</a></td>
<td>返回字符串</td>
</tr>
<tr>
<td>toUpperCase()</a></td>
<td>把字符串转换为大写</td>
</tr>
<tr>
<td>valueOf()</a></td>
<td>返回某个字符串对象的原始值</td>
</tr>
</table>

### String的HTML基本类型包装器

下边列出一系列方法，这些方法返回一个封装在适当的 HTML 标记中的字符串副本。

<table>
<tr>
<th align="left">方法</th>
<th align="left">描述</th>
</tr>
<tr>
<td>author()</a></td>
<td>创建一个 HTML 锚作为一个超文本的目标</td>
</tr>
<tr>
<td>big()</a></td>
<td>创建一个字符串用大号字体显示，就像使用 &lt;big&gt; 标签的效果</td>
</tr>
<tr>
<td>blink()</a></td>
<td>创建一个字符串闪动显示，就像使用 &lt;blink&gt; 标签的效果</td>
</tr>
<tr>
<td>bold()</a></td>
<td>创建一个字符串加粗显示，就像使用 &lt;b&gt; 标签的效果</td>
</tr>
<tr>
<td>fixed()</a></td>
<td>创建一个字符串以打字机文本显示，就像使用 &lt;tt&gt; 标签的效果</td>
</tr>
<tr>
<td>fontcolor()</a></td>
<td>创建一个字符串使用指定的颜色显示，就像使用 &lt;font color="color"&gt; 标签的效果</td>
</tr>
<tr>
<td>fontsize()</a></td>
<td>创建一个字符串使用指定的尺寸显示，就像使用 &lt;font size="size"&gt; 标签的效果</td>
</tr>
<tr>
<td>italics()</a></td>
<td>创建一个字符串使用斜体显示，就像使用 &lt;i&gt; 标签的效果</td>
</tr>
<tr>
<td>link()</a></td>
<td>创建一个 HTML 超链接,用来请求另一个 URL</td>
</tr>
<tr>
<td>small()</a></td>
<td>创建一个字符串使用小字号显示，就像使用 &lt;small&gt; 标签的效果</td>
</tr>
<tr>
<td>strike()</a></td>
<td>创建一个字符串使用删除线显示，就像使用 &lt;strike&gt; 标签的效果</td>
</tr>
<tr>
<td>sub()</a></td>
<td>创建一个字符串显示为下标，就像使用 &lt;sub&gt; 标签的效果</td>
</tr>
<tr>
<td>sup()</a></td>
<td>创建一个字符串显示为上标，就像使用 &lt;sup&gt; 标签的效果</td>
</tr>
</table>
