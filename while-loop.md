循环语句就是在满足一定条件的情况下反复执行某一个操作。循环语句可以有效减少程序的行数。  

*JavaScript* 支持所有必要的循环语句，以适用于编程过程中的所有情况。  
##While循环语句 
**While**循环是 *JavaScript* 中最基本的循环模式，下边将加以介绍。
###语法如下   

    while(expression){  
        statement  
    }  

对于 **while** 循环，当条件表达式 *expression* 的返回值为真时，则执行“{}”中的语句，当执行完“{}”中的语句后，重新判断 *expression* 的返回值，知道表达式返回值的结果为假时，退出循环。

###例子  

下面的例子说明了一个基本的 *while* 循环：  

    <script type="text/javascript">
    <!--var count = 0;
    document.write("Starting Loop"+"<br />");
    while(count < 10){
        document.write("Current Count : " + count + "<br />");
        count++;
    }
    document.write("Loop stopped!");
    //-->
    </script>


运行结果如下：  
    
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
##do...While循环语句:
**do...while** 循环和 **while** 循环非常相似，它们之间的区别是 *while* 语句为先判断条件是否成立在执行循环体，而 *do...while* 循环语句则先执行一次循环后，再判断条件是否成立。也就是说即使判断条件不成立，*do...while* 循环语句中“{}”中的程序段至少要被执行一次。  
###语法如下   
    do{  
        statement  
    }while(expression);  
注意 **do...while** 语句在结尾处多了一个分号（;）。 
###例子
下面编写一个 **do...while** 循环的例子：  

    <script type="text/javascript">
    <!--
    var count = 0;
    document.write("Starting Loop" + "<br />");
    do{
        document.write("Current Count : " + count + "<br />");
        count++;
    }while (count < 0);
    document.write("Loop stopped!");
    //-->
    </script> 


运行结果如下：   

    Starting Loop  
    Current Count : 0  
    Loop stopped!   

