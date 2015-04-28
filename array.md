## Array对象
**Array** 对象用于在单个的变量中存储多个值。   
### 语法 
创建一个 **Array** 对象：   

```
var fruits = new Array("apple","orange","mango");
```

数组的参数可以是一组字符串或整数。当你为数组构造函数指定一个数值参数时，数组的初始长度就被确定了。数组允许的最大长度是 4,294,967,295。

你可以通过简单赋值来创建一个数组，如下所示：

```
var fruits = ["apple","orange","mango"];
```

可以通过序列号（下标）来访问和设置数组内元素的值，如下所示：

- fruits[0] 是第一个元素   
- fruits[1] 是第二个元素   
- fruits[2] 是第三个元素   

### 数组属性
下边列出了数组的各个属性及对应的属性描述。  
<table border="1">
<tr>
<th>属性</th>
<th>描述</th>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_constructor.htm">constructor</a></td>
<td>返回对创建该对象的函数的引用</td>
</tr>
<tr>
<td>index</td>
<td>从零开始检索匹配的字符串</td>
</tr>
<tr>
<td>input</td>
<td>只见于通过正则表达式创建的数组</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_length.htm">length</a></td>
<td>设置或返回数组中元素的数目</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/object_prototype.htm">prototype</a></td>
<td>允许向对象添加属性和方法</td>
</tr>
</table>

### Array对象方法

下边列出了数组的一系列方法及对应的描述。  
<table border="1">
<tr>
<th>方法</th>
<th>描述</th>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_concat.htm">concat()</a></td>
<td>连接两个或更多的数组，并返回结果</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_every.htm">every()</a></td>
<td>对数组元素应用指定的函数进行判断，当且仅当所有返回值为 true，返回 true，否则返回 false</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_filter.htm">filter()</a></td>
<td>创建一个新数组，数组中的元素是原数组中满足过滤函数返回值为空的元素</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_foreach.htm">forEach()</a></td>
<td>从头到尾遍历数组，为每个元素调用制定的函数</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_indexof.htm">indexOf()</a></td>
<td>从头到尾检索，返回给定元素在数组中的索引</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_join.htm">join()</a></td>
<td>把数组的所有元素放入一个字符串。元素通过制定的分隔符进行分割</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_lastindexof.htm">lastIndexOf()</a></td>
<td>从尾到头检索，返回给定元素在数组中的索引</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_map.htm">map()</a></td>
<td>创建一个新数组，用来存储原数组中每个元素调用指定函数的返回值</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_pop.htm">pop()</a></td>
<td>删除并返回数组的最后一个元素</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_push.htm">push()</a></td>
<td>向数组的末尾添加一个或更多元素，并返回新的长度。</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_reduce.htm">reduce()</a></td>
<td>同时对数组中的两个值应用一个函数，使减少到一个单一值（从头到尾）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_reduceright.htm">reduceRight()</a></td>
<td>同时对数组中的两个值应用一个函数，使减少到一个单一值（从尾到头）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_reverse.htm">reverse()</a></td>
<td>颠倒数组中元素的顺序</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_shift.htm">shift()</a></td>
<td>删除并返回数组的第一个元素</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_slice.htm">slice()</a></td>
<td>从某个已有的数组返回选定的元素</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_some.htm">some()</a></td>
<td>对数组元素应用指定的函数进行判断，只有有一个返回值为 true，返回 true，否则返回 false</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_tosource.htm">toSource()</a></td>
<td>返回该对象的源代码</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_sort.htm">sort()</a></td>
<td>将数组中的元素进行排序</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_splice.htm">splice()</a></td>
<td>在数组中插入或删除元素</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_tostring.htm">toString()</a></td>
<td>把数组转换为字符串，并返回结果</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/array_unshift.htm">unshift()</a></td>
<td>将一个或多个元素添加到数组的前面,并返回新数组的长度。</td>
</tr>
</table>