## 日期对象

Date 对象是 JavaScript 语言的一个内置数据类型。Date 对象用 **new Date()** 创建，如下所示。  

Date 对象一旦被创建，就可以使用许多方法来操作它。大多数方法只允许获取并设置对象的年、月、日、小时、分钟、秒、和毫秒字段，可以使用当地时间或世界标准时间（UTC，GMT）时间。   

ECMAScript 标准要求的 Date 对象能够代表任何日期和时间，在1/1/1970之前或之后的 1 亿天内精确到毫秒。这是一个正负 273785 年的变化范围，所以 JavaScript 能够表示直到 275755 年的日期和时间。

### 语法

Date() 构造函数有几种不同的形式：

```
    new Date() 
    new Date(milliseconds)  
    new Date(datestring)   
    new Date(year,month,date[,hour,minute,second,millisecond])
```

**注意：** 方括号内的参数是可选的。
  
下面是参数描述：  
- **No Argument：** 不带参数，Date() 构造函数创建一个日期对象，设置为当前日期和时间。      
- **milliseconds：** 当传递一个数字作为参数，它作为表示日期中毫秒的内部数字，作为 getTime() 方法的返回值中的毫秒。例如，通过传递参数 5000 创建一个日期对象，代表 1/1/1970 午夜过去 5 秒钟。 
- **datestring：** 当传递一个字符串作为参数，它必须是一个日期形式的字符串，即可以被 Date.parse() 方法接收的格式。          
- **7 agrument：** 对于上面给出的最后一种形式的构造函数，下面是每个参数的描述。

    1. **year：** 整数，表示年。为了兼容性(为了避免Y2K问题)，应该完整地指定年；使用 1998而不是 98。   
    2. **month：**整数，表示月。从 0（表示一月）开始到 11（表示十二月）。   
    3. **date：** 整数，表示一个月的某一天。   
    4. **hour：** 整数，表示一天的某一个小时（24小时制）。   
    5. **minute：** 整数，表示时间计数的分钟片段。   
    6. **second：** 整数，表示时间计数的秒片段。    
    7. **milliseconds：** 整数，表示时间计数的毫秒片段。  
    
### Date属性

下边列出了日期的各个属性及对应的属性描述。 

<table >
<tr>
<th align="left">属性</th>
<th align="left">描述</th>
</tr>
<tr>
<td>constructor</td>
<td>返回对创建该对象的函数的引用</td>
</tr>
<tr>
<td>prototype</td>
<td>允许向对象添加属性和方法</td>
</tr>
</table>

### Date方法

下边列出了日期的一系列方法及对应的描述。 

<table>
<tr>
<th align="left">方法</th>
<th align="left">描述</th>
</tr>
<tr>
<td>Date()</td>
<td>返回当日的日期和时间</td>
</tr>
<tr>
<td>getDate()</td>
<td>根据本地时从Date对象返回一个月中的某一天（1 ~ 31）</td>
</tr>
<tr>
<td>getDay()</td>
<td>根据本地时从Date对象返回一周中的某一天（1 ~ 6）</td>
</tr>
<tr>
<td>getFullYear()</td>
<td>根据本地时从 Date 对象以四位数字返回年份</td>
</tr>
<tr>
<td>getHours()</td>
<td>根据本地时返回 Date 对象的小时 (0 ~ 23)</td>
</tr>
<tr>
<td>getMilliseconds()</td>
<td>根据本地时返回 Date 对象的毫秒(0 ~ 999)</td>
</tr>
<tr>
<td>getMinutes()</td>
<td>根据本地时返回 Date 对象的分钟 (0 ~ 59)</td>
</tr>
<tr>
<td>getMonth()</td>
<td>根据本地时从Date对象返回月份（1 ~ 11）</td>
</tr>
<tr>
<td>getSeconds()</td>
<td>根据本地时返回 Date 对象的秒数 (0 ~ 59)</td>
</tr>
<tr>
<td>getTime()</td>
<td>根据本地时返回 1970 年 1 月 1 日至今的毫秒数</td>
</tr><tr>
<td>getTimezoneOffset()</td>
<td>返回本地时间与格林威治标准时间 (GMT) 的分钟差</td>
</tr>
<tr>
<td>getUTCDate()</td>
<td>根据世界时从 Date 对象返回月中的一天 (1 ~ 31)</td>
</tr>
<tr>
<td>getUTCDay()</td>
<td>根据世界时从 Date 对象返回周中的一天 (0 ~ 6)</td>
</tr>
<tr>
<td>getUTCFullYear()</td>
<td>根据世界时从 Date 对象返回四位数的年份</td>
</tr>
<tr>
<td>getUTCHours()</td>
<td>根据世界时返回 Date 对象的小时 (0 ~ 23)</td>
</tr>
<tr>
<td>getUTCMilliseconds()</td>
<td>根据世界时返回 Date 对象的毫秒(0 ~ 999)</td>
</tr>
<tr>
<td>getUTCMinutes()</td>
<td>根据世界时返回 Date 对象的分钟 (0 ~ 59)</td>
</tr>
<tr>
<td>getUTCMonth()</td>
<td>根据世界时从 Date 对象返回月份 (0 ~ 11)</td>
</tr>
<tr>
<td>getUTCSeconds()</td>
<td>根据世界时返回 Date 对象的秒钟 (0 ~ 59)</td>
</tr>
<tr>
<td>getYear()</td>
<td>弃用,返回在指定的日期根据当地时间。使用getFullYear()代替。</td>
</tr>
<tr>
<td>setDate()</td>
<td>根据本地时设置 Date 对象中月的某一天 (1 ~ 31)</td>
</tr>
<tr>
<td>setFullYear()</td>
<td>根据本地时设置 Date 对象中的年份（四位数字）</td>
</tr>
<tr>
<td>setHours()</td>
<td>根据本地时设置 Date 对象中的小时 (0 ~ 23)</td>
</tr>
<tr>
<td>setMilliseconds()</td>
<td>根据本地时设置 Date 对象中的毫秒 (0 ~ 999)</td>
</tr>
<tr>
<td>setMinutes()</td>
<td>根据本地时设置 Date 对象中的分钟 (0 ~ 59)</td>
</tr>
<tr>
<td>setMonth()</td>
<td>根据本地时设置 Date 对象中月份 (0 ~ 11)</td>
</tr>
<tr>
<td>setSeconds()</td>
<td>根据本地时设置 Date 对象中的秒钟 (0 ~ 59)</td>
</tr>
<tr>
<td>setTime()</td>
<td>根据本地时以毫秒设置 Date 对象</td>
</tr>
<tr>
<td>setUTCDate()</td>
<td>根据世界时设置 Date 对象中月份的一天 (1 ~ 31)</td>
</tr>
<tr>
<td>setUTCFullYear()</td>
<td>根据世界时设置 Date 对象中的年份（四位数字）</td>
</tr>
<tr>
<td>setUTCHours()</td>
<td>根据世界时设置 Date 对象中的小时 (0 ~ 23)</td>
</tr>
<tr>
<td>setUTCMilliseconds()</td>
<td>根据世界时设置 Date 对象中的毫秒 (0 ~ 999)</td>
</tr>
<tr>
<td>setUTCMinutes()</td>
<td>根据世界时设置 Date 对象中的分钟 (0 ~ 59)</td>
</tr>
<tr>
<td>setUTCMonth()</td>
<td>根据世界时设置 Date 对象中的月份 (0 ~ 11)</td>
</tr>
<tr>
<td>setUTCSeconds()</td>
<td>根据世界时设置 Date 对象中的秒钟 (0 ~ 59)</td>
</tr>
<tr>
<td>setYear()</td>
<td>弃用,设置为指定的日期根据当地时间。使用 setFullYear() 代替。</td>
</tr>
<tr>
<td>toDateString()</td>
<td>把 Date 对象的日期部分转换为字符串</td>
</tr>
<tr>
<td>toGMTString()</td>
<td>弃用,将日期转换为一个字符串,使用互联网格林尼治时间约定。使用 toUTCString() 代替。</td>
</tr>
<tr>
<td>toLocalDateString()</td>
<td>根据本地时间格式，把 Date 对象的日期部分转换为字符串</td>
</tr>
<tr>
<td>toLocalFormat()</td>
<td>将日期转换为一个字符串,使用格式化字符串。</td>
</tr>
<tr>
<td>toLocalString()</td>
<td>根据本地时间格式，把 Date 对象转换为字符串</td>
</tr>
<tr>
<td>toLocalTimeString()</td>
<td>根据本地时间格式，把 Date 对象的时间部分转换为字符串</td>
</tr>
<tr>
<td>toSource()</td>
<td>返回一个字符串代表一个等价的日期对象的源码,您可以使用这个值来创建一个新的对象</td>
</tr>
<tr>
<td>toString()</td>
<td>把 Date 对象转换为字符串</td>
</tr>
<tr>
<td>toTimeString()</td>
<td>把 Date 对象的时间部分转换为字符串</td>
</tr>
<tr>
<td>toUCTString()</td>
<td>根据世界时，把 Date 对象转换为字符串</td>
</tr>
<tr>
<td>valueOf()</td>
<td>返回 Date 对象的原始值</td>
</tr>
</table>

### Date静态方法

<table>
<tr>
<th align="left">方法</th>
<th align="left">描述</th>
</tr>
<tr>
<td>Date.parse()</td>
<td>返回 1970 年 1 月 1 日午夜到指定日期（字符串）的毫秒数</td>
</tr>
<tr>
<td>Date.UTC()</td>
<td>根据世界时返回 1970 年 1 月 1 日 到指定日期的毫秒数</td>
</tr>
</table>
