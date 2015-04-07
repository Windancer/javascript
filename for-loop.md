我们已经学习了几种不同的 **while** 循环，这一章我们来学习另一种更普及的循环 **for** 循环。
##for循环语句: 
**for** 循环是一种最简洁的循环模式，包括三个重要部分：  

- *initialize* ：初始化表达式,初始化计数器一个初始值，在循环开始前计算初始状态。  
- *test condition* ：判断条件表达式，判断给定的状态是否为真。如果条件为真，则执行循环体“{}”中的代码，否则跳出循环。  
- *iteration statement* ：循环操作表达式，改变循环条件，修改计数器的值。  

可以将这三个部分放在同一行，用分号隔开。
###语法如下   
    for(initialize;test condition;iteration statement)  
    {  
        statement;  
    }
###例子  
下面的例子说明了一个基本的 *for* 循环：
    
    <script type="text/javascript">
    <!--
    var count;
    document.write("Starting Loop" + "<br />");
    for(count = 0; count < 10; count++){
        document.write("Current Count : " + count );
        document.write("<br />");
    }
    document.write("Loop stopped!");
    //-->
    </script>  
下面就是本实例的运行结果，可见这和 **while** 循环的运行结果一样： 

    Starting Loop
    Current Count : 0
    Current Count : 1
    Current Count : 2
    Current Count : 3
    Current Count : 4
    Current Count : 5
    Current Count : 6
    Current Count : 7
    Current Count : 8
    Current Count : 9
    Loop stopped!  
 
为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_10)。
   
