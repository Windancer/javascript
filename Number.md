# JavaScript - 数字对象

**Number** 对象表示数值日期，整数或浮点数。一般情况下，你不需要担心 **Number** 对象，因为浏览器自动将数字文本转换为数字类的实例。  

## 语法：  
 
创建一个 **Number** 对象：  

    var val = new Number(number);

如果该参数不能转换为数字，它将返回为 NaN(Not-a-Number)。

## 数字属性：

这里有每个属性和它的描述的列表。

<table border="1">  
<tr>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_max_value.htm">MAX_VALUE</a></td>
<td>最大的可能值在 JavaScript 中的数量可以有 1.7976931348623157E+308 </td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_min_value.htm">MIN_VALUE</a></td>
<td>最小的可能值在 JavaScript 中的数量可以有 5E-324</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_nan.htm">NaN</a></td>
<td>等价于一个值不是一个数字。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_negative_infinity.htm">NEGATIVE INFINITY</a></td>
<td>比 MIN-VALUE 小的值。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_positive_infinity.htm">POSITIVE_INFINITY</a></td>
<td>比 MAX-VALUE 大的值。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/object_prototype.htm">prototype</a></td>
<td>数字对象的静态属性。使用原型对象的属性来给当前文档中的数字对象分配新的属性和方法。</td>
</tr>
</table>


## 数字方法：

数字对象只包含每个对象定义的一部分默认方法。

<table border="1">
<tr>
<th>Method</th>
<th>Description</th>
</tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_constructor.htm">constructor()</a></td>
<td>返回创建此对象的实例的函数。默认这是数字对象。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_toexponential.htm">toExponential()</a></td>
<td>将一个数字强制以指数表示法显示，即使这个数字在 JavaScript 通常规定使用标准符号表示的范围之内。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_tofixed.htm">toFixed()</a></td>
<td>格式一个数为小数点右边有特定位数的小数。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_tolocalestring.htm">toLocaleString()</a></td>
<td>返回当前数字的字符串值版本的格式可能根据浏览器的区域设置不同而发生变化。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_toprecision.htm">toPrecision()</a></td>
<td>
定义了总共有多少有多少为来显示一个数（包括小数点左边和右边的数）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_tostring.htm">toString()</a></td>
<td>返回数的值的字符串表示形式。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/number_valueof.htm">valueOf()</a></td>
<td>返回数的值。</td>
</tr>
</table>












