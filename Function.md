# JavaScript内置函数 #

## 数值方法 ##


数值对象仅包含了几个任何对象均定义的默认方法



<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>constructor()</td> <td>返回创建该对象实例的函数。默认是数值对象。</td> 
</tr>

</tr>
<tr>
<td>toExponential()</td> <td>强制将数值以指数形式显示。</td> 
</tr>

</tr>
<tr>
<td>toFixed()</td> <td>可把 Number 四舍五入为指定小数位数的数字。</td> 
</tr>

</tr>
<tr>
<td>toLocaleString()</td> <td>以字符串的形式返回当前对象的值。该字符串适用于宿主环境的当前区域设置。</td> 
</tr>

</tr>
<tr>
<td>toPrecision()</td> <td>定义显示一个数多少位数（包括位小数的左和右）</td> 
</tr>

</tr>
<tr>
<td>toString()</td> <td>返回该数值的字符串格式</td> 
</tr>

</tr>
<tr>
<td>valueOf()</td> <td>返回数值</td> 
</tr>

</tbody>
</table>

## 布尔方法 ##

如下为相关方法及描述的列表：






<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>toSource()</td> <td>返回一个包含布尔对象的源字符串;可以使用这个字符串创建一个等价的对象。</td> 
</tr>

</tr>
<tr>
<td>toString()</td> <td>按照布尔结果返回“true”或
“fales”。</td> 
</tr>

</tr>
<tr>
<td>valueOf()</td> <td>返回布尔对象的原始值。</td> 
</tr>

</tbody>
</table>

## 字符串方法 ##
如下为相关方法及描述的列表：  


<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>charAt()</td> <td>返回指定位置的字符。</td> 
</tr>

</tr>
<tr>
<td>charCodeAt()</td> <td>返回指定位置字符的数值。</td> 
</tr>

</tr>
<tr>
<td>concat()</td> <td>返回布尔对象的原始值。</td> 
</tr>

</tr>
<tr>
<td>indexOf()</td> <td>返回匹配子字符串第一次出现的位置，如果不存在就返回-1。</td> 
</tr>

</tr>
<tr>
<td>lastIndexOf()</td> <td>返回匹配子字符串最后一次出现的位置，如果不存在就返回-1。</td> 
</tr>

</tr>
<tr>
<td>localeCompare()</td> <td>比较两个字符串,并返回以数字形式表示的比较结果。</td> 
</tr>

</tr>
<tr>
<td>length()</td> <td>返回字符串的长度。</td> 
</tr>

</tr>
<tr>
<td>match()</td> <td>用于匹配正则表达式。</td> 
</tr>

</tr>
<tr>
<td>replace()</td> <td>通过与正则表达式找到子串位置，并替换为新指定的字符串。</td> 
</tr>

</tr>
<tr>
<td>search()</td> <td>执行与一个正则表达式进行的搜索。</td> 
</tr>

</tr>
<tr>
<td>slice()</td> <td>提取并返回一个子串。</td> 
</tr>

</tr>
<tr>
<td>split()</td> <td>将字符串分割成多个子串，并存储进字符串数组。</td> 
</tr>

</tr>
<tr>
<td>substr()</td> <td>返回字符串中指定位置，指定长度的子串。</td> 
</tr>

</tr>
<tr>
<td>toLocaleLowerCase()</td> <td>大写字符转为小写，同时尊重当前语言环境。</td> 
</tr>
</tr>
<tr>
<td>toLocaleUpperCase()</td> <td>小写字符转为大写，同时尊重当前语言环境。</td> 
</tr>
</tr>
<tr>
<td>toLowerCase()</td> <td>大写字符转为小写。</td> 
</tr>
</tr>
<tr>
<td>toString()</td> <td>返回表示该对象的一个字符串。</td> 
</tr>
</tr>
<tr>
<td>toUpperCase()</td> <td>小写字符转为大写。</td> 
</tr>
</tr>
<tr>
<td>valueOf()</td> <td>返回指定对象的原始数值。</td> 
</tr>

</tbody>
</table>

## HTML字符串格式化工具 ##

<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>anchor()</td> <td>创建一个HTML锚作为一个超文本的目标。</td> 
</tr>

</tr>
<tr>
<td>big()</td> <td>创建一个以“大”字体表示的字符串，好比置于< big >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>blink()</td> <td>创建一个闪烁的字符串，好比置于< blink >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>bold()</td> <td>创建一个粗体显示的字符串，好比置于< b >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>fixed()</td> <td>创建一个打字机字体显示的字符串，好比置于< tt >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>fontcolor()</td> <td>创建一个特定字体颜色显示的字符串，好比置于< font color="color" >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>fontsize()</td> <td>创建一个特定字体大小显示的字符串，好比置于< font size="size" >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>italics()</td> <td>创建一个斜体显示的字符串，好比置于< i >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>link()</td> <td>创建HTML超级链接。</td> 
</tr>

</tr>
<tr>
<td>small()</td> <td>创建一个小字体显示的字符串，好比置于< small >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>strike()</td> <td>创建一个加了删除线显示的字符串，好比置于< strike >标签中一样。</td> 
</tr>


</tr>
<tr>
<td>sub()</td> <td>以下标的方式显示，好比置于< sub >标签中一样。</td> 
</tr>

</tr>
<tr>
<td>sup()</td> <td>以上标的方式显示，好比置于< sup >标签中一样。</td> 
</tr>

</tbody>
</table>

## 数组方法 ##
如下为相关方法及描述的列表：


<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>concat()</td> <td>返回两个数据经过联接后的数组。</td> 
</tr>

</tr>
<tr>
<td>every()</td> <td>如何数组内的元素均满足某测试函数，那么就返回true。</td> 
</tr>

</tr>
<tr>
<td>filter()</td> <td>原来的数组中能过通过过滤器的元素组成一个新的数组返回。</td> 
</tr>


</tr>
<tr>
<td>forEach()</td> <td>调用一个函数来处理数组中的每个元素。</td> 
</tr>


</tr>
<tr>
<td>indexOf()</td> <td>返回与指定元素相匹配的第一个位置，如果不存在就返回-1</td> 
</tr>


</tr>
<tr>
<td>join()</td> <td>连接数组中所有的元素，返回一个字符串</td> 
</tr>


</tr>
<tr>
<td>lastIndexOf()</td> <td>返回与指定元素相匹配的最后一个位置，如果不存在就返回-1。</td> 
</tr>


</tr>
<tr>
<td>map()</td> <td>调用一个函数处理数组中的每一个元素，将生成的结果组成一个新的数组，并返回</td> 
</tr>


</tr>
<tr>
<td>pop()</td> <td>返回数组中的最后一个元素，并删除。</td> 
</tr>


</tr>
<tr>
<td>push()</td> <td>在数组的最后增加一个元素，并返回新数组的长度</td> 
</tr>


</tr>
<tr>
<td>reduce()</td> <td>对数组中的所有元素（从左到右）调用指定的回调函数。 该回调函数的返回值为累积结果，并且此返回值在下一次调用该回调函数时作为参数提供。</td> 
</tr>


</tr>
<tr>
<td>reduceRight()</td> <td>对数组中的所有元素（从右到左）调用指定的回调函数。 该回调函数的返回值为累积结果，并且此返回值在下一次调用该回调函数时作为参数提供。</td> 
</tr>


</tr>
<tr>
<td>reverse()</td> <td>反转数组元素的顺序——第一个成为最后一个,最后成为第一。</td> 
</tr>


</tr>
<tr>
<td>shift()</td> <td>删除数组的第一个元素并返回。</td> 
</tr>


</tr>
<tr>
<td>slice()</td> <td>提取一段数组并返回一个新的数组</td> 
</tr>

</tr>
<tr>
<td>some()</td> <td>,如果存在一个元素满足所提供的测试函数，就返回true。</td> 
</tr>


</tr>
<tr>
<td>toSource()</td> <td>代表一个对象的源代码。</td> 
</tr>


</tr>
<tr>
<td>sort()</td> <td>对数组中的元素排序。</td> 
</tr>


</tr>
<tr>
<td>splice()</td> <td>增删数组中的元素。</td> 
</tr>

</tr>
<tr>
<td>toString()</td> <td>返回一个表示数组及其元素的字符串。</td> 
</tr>

</tr>
<tr>
<td>unshift()</td> <td>在数组的首部添加新的元素，并且返回新数组的长度</td> 
</tr>



</tbody>
</table>

## 时期方法 ##

如下为相关方法及描述的列表：






<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>Date()</td> <td>返回今天的日期及时间。</td> 
</tr>

</tr>
<tr>
<td>getDate()</td> <td>按照本地模式返回指定日期是哪日。</td> 
</tr>

</tr>
<tr>
<td>getDay()</td> <td>按照本地模式返回指定日期是周几。</td> 
</tr>

</tr>
<tr>
<td>getFullYear()</td> <td>按照本地模式返回指定日期是哪一年。</td> 
</tr>

</tr>
<tr>
<td>getMilliseconds()</td> <td>按照本地模式返回指定日期是几毫秒。</td> 
</tr>

</tr>
<tr>
<td>getMinutes()</td> <td>按照本地模式返回指定日期是几分。</td> 
</tr>

</tr>
<tr>
<td>getMonth()</td> <td>按照本地模式返回指定日期的月份。</td> 
</tr>

</tr>
<tr>
<td>getSeconds()</td> <td>按照本地模式返回指定日期是几秒。</td> 
</tr>

</tr>
<tr>
<td>getTime()</td> <td>按照本地模式当前的格林威治时间。</td> 
</tr>

</tr>
<tr>
<td>getTimezoneOffset()</td> <td>以分钟为单位返回时间偏差。</td> 
</tr>

</tr>
<tr>
<td>getUTCDate()</td> <td>按照世界统一时间返回指定日期是几号。</td> 
</tr>


</tr>
<tr>
<td>getUTCDay()</td> <td>按照世界统一时间返回指定日期是周几。</td> 
</tr>

</tr>
<tr>
<td>getUTCFullYear()</td> <td>按照世界统一时间返回指定日的年份。</td> 
</tr>

</tr>
<tr>
<td>getUTCHours()</td> <td>按照世界统一时间返回指定日期是几时。</td> 
</tr>

</tr>
<tr>
<td>getUTCMilliseconds()</td> <td>按照世界统一时间返回指定日期的毫秒数。</td> 
</tr>

</tr>
<tr>
<td>getUTCMinutes()</td> <td>按照世界统一时间返回指定日期的分钟数。</td> 
</tr>

</tr>
<tr>
<td>getUTCMonth()</td> <td>按照世界统一时间返回指定日期的月份。</td> 
</tr>

</tr>
<tr>
<td>getUTCSeconds()</td> <td>按照世界统一时间返回指定日期的秒数。</td> 
</tr>

</tr>
<tr>
<td>setDate()</td> <td>按照本地模式设置日期。</td> 
</tr>

</tr>
<tr>
<td>setFullYear()</td> <td>按照本地模式设置年份。</td> 
</tr>

</tr>
<tr>
<td>setHours()</td> <td>按照本地模式设置小时。</td> 
</tr>

</tr>
<tr>
<td>setMilliseconds()</td> <td>按照本地模式设置毫秒数。</td> 
</tr>

</tr>
<tr>
<td>setMinutes()</td> <td>按照本地模式设置分钟数。</td> 
</tr>

</tr>
<tr>
<td>setMonth()</td> <td>按照本地模式设置月份。</td> 
</tr>

</tr>
<tr>
<td>setSeconds()</td> <td>按照本地模式设置秒数。</td> 
</tr>

</tr>
<tr>
<td>setTime()</td> <td>按照格林威治格式设置毫秒数。</td> 
</tr>

</tr>
<tr>
<td>setUTCDate()</td> <td>按照世界统一时间设置日期。</td> 
</tr>

</tr>
<tr>
<td>setUTCFullYear()</td> <td>按照世界统一时间设置年份。</td> 
</tr>

</tr>
<tr>
<td>setUTCHours()</td> <td>按照世界统一时间设置小时数。</td> 
</tr>

</tr>
<tr>
<td>setUTCMilliseconds()</td> <td>按照世界统一时间设置毫秒数。</td> 
</tr>

</tr>
<tr>
<td>setUTCMinutes()</td> <td>按照世界统一时间设置分钟数。</td> 
</tr>

</tr>
<tr>
<td>setUTCMonth()</td> <td>按照世界统一时间设置月份。</td> 
</tr>

</tr>
<tr>
<td>setUTCSeconds()</td> <td>按照世界统一时间设置秒数。</td> 
</tr>

</tr>
<tr>
<td>toDateString()</td> <td>返回日期的字符串。</td> 
</tr>

</tr>
<tr>
<td>toLocaleDateString()</td> <td>按照本地模式，返回日期的字符串。</td> 
</tr>


</tr>
<tr>
<td>toLocaleFormat()</td> <td>使用格式字符串，将日期转换为一个字符串。</td> 
</tr>

</tr>
<tr>
<td>toLocaleString()</td> <td>使用当前语言环境的约定将日期转换为一个字符串。</td> 
</tr>

</tr>
<tr>
<td>toLocaleTimeString()</td> <td>返回日期的“时间”部分作为一个字符串,使用当前语言环境的约定。</td> 
</tr>

</tr>
<tr>
<td>toSource()</td> <td>返回一个字符串代表一个等价的日期对象的来源,您可以使用这个值来创建一个新的对象。</td> 
</tr>

</tr>
<tr>
<td>toString()</td> <td>返回一个字符串代表指定的日期对象。</td> 
</tr>

</tr>
<tr>
<td>toTimeString()</td> <td>返回日期的“时间”部分以字符串形式。</td> 
</tr>

</tr>
<tr>
<td>toUTCString()</td> <td>使用通用时间约定，将日期转换为一个字符串。</td> 
</tr>

</tr>
<tr>
<td>valueOf()</td> <td>返回日期对象的原始值。</td> 
</tr>

</tbody>
</table>  


## 日期静态方法 ##

如下为相关方法及描述的列表：






<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>Date.parse( )</td> <td>解析并返回日期和时间的字符串表示的内部毫秒表示日期。</td> 
</tr>

</tr>
<tr>
<td>Date.UTC( )</td> <td>返回指定的毫秒表示UTC日期和时间。</td> 
</tr>



</tbody>
</table>

## 数学方法 ##


如下为相关方法及描述的列表：


<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>abs()</td> <td>返回数值的绝对值。</td> 
</tr>

</tr>
<tr>
<td>acos()</td> <td>返回一个数值的arccos值。</td> 
</tr>

</tr>
<tr>
<td>asin()</td> <td>返回一个数值的arcsin值。</td> 
</tr>

</tr>
<tr>
<td>atan()</td> <td>返回一个数值的arctan值。</td> 
</tr>

</tr>
<tr>
<td>ceil()</td> <td>返回大于或等于整数最小的一个数字。</td> 
</tr>

</tr>
<tr>
<td>cos()</td> <td>返回一个数值的cos值。</td> 
</tr>

</tr>
<tr>
<td>exp()</td> <td>返回指数。</td> 
</tr>

</tr>
<tr>
<td>floor()</td> <td>返回小于等于一个数的最大数。</td> 
</tr>

</tr>
<tr>
<td>log()</td> <td>返回一个数值以e为底的对数。</td> 
</tr>

</tr>
<tr>
<td>max()</td> <td>返回最大值。</td> 
</tr>

</tr>
<tr>
<td>min()</td> <td>返回最小值。</td> 
</tr>

</tr>
<tr>
<td>pow()</td> <td>返回以e为底的幂。</td> 
</tr>

</tr>
<tr>
<td>random()</td> <td>返回0和1之间的一个伪随机数。</td> 
</tr>

</tr>
<tr>
<td>round()</td> <td>返回四舍五入后的值。</td> 
</tr>

</tr>
<tr>
<td>sin()</td> <td>返回sin值。</td> 
</tr>

</tr>
<tr>
<td>sqrt()</td> <td>返回一个整数的平方根。</td> 
</tr>

</tr>
<tr>
<td>tan()</td> <td>返回一个数值的tan值。</td> 
</tr>

</tr>
<tr>
<td>toSource()</td> <td>返回字符串“Manth”。</td> 
</tr>

</tbody>
</table>
## 正则表达式方法 ##


如下为相关方法及描述的列表：






<table>
<tbody>
<tr>
<th>方法</th>
<th>描述</th>

</tr>
<tr>
<td>exec()</td> <td>执行一个字符串的搜索匹配。</td> 
</tr>

</tr>
<tr>
<td>test()</td> <td>测试匹配的字符串参数。</td> 
</tr>

</tr>
<tr>
<td>toSource（）</td> <td>返回一个对象文字代表指定的对象;您可以使用这个值来创建一个新的对象。</td> 
</tr>

</tr>
<tr>
<td>toString（）</td> <td>返回一个字符串代表指定的对象。</td> 
</tr>

</tbody>
</table>