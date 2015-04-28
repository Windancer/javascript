## Math对象
**Math** 对象提供针对数学常量的属性、方法的和功能。

不同于其他的全局对象，Math 不是一个构造函数。Math 的所有属性和方法都是静态的，无需创建它，通过把 Math 作为对象使用就可以调用其所有属性和方法。

因此，可以定义常量 pi 为 **Math.PI**，也可以调用sin函数 **Math.sin(x)**，其中 *x* 是方法的参数。
### 语法
这是 Math 中调用属性和方法的简单语法。   

	var pi_val = Math.PI;
	var sine_val = Math.sin(30);

### Math属性
这是 Math 的各个属性及对应的属性描述的列表。 
<table border="1">
<tr>
<th>属性</th>
<th>描述</th>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_e.htm">E</a></td>
<td>返回算术常量 e，即自然对数的底数（约等于 2.718）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_ln2.htm">LN2</a></td>
<td>返回 2 的自然对数（约等于 0.693）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_ln10.htm">LN10</a></td>
<td>返回 10 的自然对数（约等于 2.302）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_log2e.htm">LOG2E</a></td>
<td>返回以 2 为底的对数（约等于 1.414）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_log10e.htm">LOG10E</a></td>
<td>返回以 10 为底的对数（约等于 0.434）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_pi.htm">PI</a></td>
<td>返回圆周率（约等于 3.14159）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_sqrt1_2.htm">SQRT1_2</a></td>
<td>返回 2 的平方根的倒数（约等于 0.707）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_sqrt2.htm">SQRT2</a></td>
<td>返回2的平方根（约等于 1.414）</td>
</tr>
</table>
### Math方法
这是 Math 的各个方法及对应的属性描述的列表。
<table border="1">
<tr>
<th>属性</th>
<th>描述</th>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_abs.htm">abs()</a></td>
<td>返回数的绝对值</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_acos.htm">acos()</a></td>
<td>返回数的反余弦值</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_asin.htm">asin()</a></td>
<td>返回数的反正弦值</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_atan.htm">atan()</a></td>
<td>以介于 -PI/2 与 PI/2 弧度之间的数值来返回 x 的反正切值</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_atan2.htm">atan2()</a></td>
<td>返回从 x 轴到点 (x,y) 的角度（介于 -PI/2 与 PI/2 弧度之间）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_atan.htm">ceil()</a></td>
<td>对数进行上舍入</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_cos.htm">cos()</a></td>
<td>返回数的余弦</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_exp.htm">exp()</a></td>
<td>返回 e 的指数</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_floor.htm">floor()</a></td>
<td>对数进行下舍入</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_log.htm">log()</a></td>
<td>返回数的自然对数（底为e）</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_max.htm">max()</a></td>
<td>返回 x 和 y 中的最高值</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_min.htm">min()</a></td>
<td>返回 x 和 y 中的最低值</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_pow.htm">pow()</a></td>
<td>返回 x 的 y 次幂</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_random.htm">random()</a></td>
<td>返回 0~1 之间的随机数</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_round.htm">round()</a></td>
<td>把数四舍五入为最接近的整数</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_sin.htm">sin()</a></td>
<td>返回数的正弦</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_sqrt.htm">sqort()</a></td>
<td>返回数的平方根</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_tan.htm">tan()</a></td>
<td>返回角的正切</td>
</tr>
<tr>
<td><a href="http://www.tutorialspoint.com/javascript/math_tosource.htm">toSource()</a></td>
<td>返回该对象的源代码</td>
</tr>
</table> 