##JavaScript - 表单有效性验证

当用户输完了所有必要的数据并且点击了提交按钮，接着就会进行表单的有效性进行验证，表单验证通常发生在服务器端。如果用户输入的一些数据存在错误，或者没有输入数据，服务器就必须返回给客户端所有的数据，并且要求用户重新提交正确的数据。这个过程确实是处理比较费时，而且给服务器造成很大压力。

JavaScript 提供了一种方式在客户端提交数据到服务器之前验证表单数据的有效性。通常利用两个函数来验证表单数据的有效性。

- 基本有效性验证： 首先，表单必须确保所有需要输入的数据的区域有数据。这个需要循环的对表单中需要输入数据的区域进行检验数据是否为空。
- 数据格式验证： 其次，被输入的数据必须要检查它的格式和值是否正确。这就需要更多的逻辑测试。

我们举个例子来说明有效性验证的过程。如下是个简单的例子：

	<html>
	<head>
	<title>Form Validation</title>
	<script type="text/javascript">
	<!--
	// Form validation code will come here.
	//-->
	</script>
	</head>
	<body>
	<form action="/cgi-bin/test.cgi" name="myForm"  
          onsubmit="return(validate());">
	<table cellspacing="2" cellpadding="2" border="1">
	<tr>
	<td align="right">Name</td>
	<td><input type="text" name="Name" /></td>
	</tr>
	<tr>
	<td align="right">EMail</td>
	<td><input type="text" name="EMail" /></td>
	</tr>
	<tr>
	<td align="right">Zip Code</td>
	<td><input type="text" name="Zip" /></td>
	</tr>
	<tr>
	<td align="right">Country</td>
	<td>
	<select name="Country">
	<option value="-1" selected>[choose yours]</option>
	<option value="1">USA</option>
	<option value="2">UK</option>
	<option value="3">INDIA</option>
	</select>
	</td>
	</tr>
	<tr>
	<td align="right"></td>
	<td><input type="submit" value="Submit" /></td>
	</tr>
	</table>
	</form>
	</body>
	</html>

###基本表单验证

首先我们会展示如何进行基本的表单有效性验证。上面的代码中我们调用了 **validate()** 函数验证数据有效性，当事件 **onsubmit** 发生的时候。下面是对 validate() 函数的实现。


	<script type="text/javascript">
	<!--
	// Form validation code will come here.
	function validate()
	{
 
	   if( document.myForm.Name.value == "" )	
	   {
    	 alert( "Please provide your name!" );
		 document.myForm.Name.focus() ;
     	 return false;
		}
	 if( document.myForm.EMail.value == "" )
	{
     alert( "Please provide your Email!" );
     document.myForm.EMail.focus() ;
     return false;
	}
	if( document.myForm.Zip.value == "" ||
           isNaN( document.myForm.Zip.value ) ||
           document.myForm.Zip.value.length != 5 )
	{
     alert( "Please provide a zip in the format #####." );
     document.myForm.Zip.focus() ;
     return false;
	}
	if( document.myForm.Country.value == "-1" )
	{
     alert( "Please provide your country!" );
     return false;
	}
	return( true );
	}
	//-->
	</script>

为了更好理解此处的内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_42)。

###数据格式有效性验证

接下来我们将会演示在将数据提交到服务器端之前我们如何验证数据的有效性。

这个例子演示如何验证用户输入的邮箱地址的有效性，因为输入的邮箱格式中必须包含 @ 符号和一个点号(.)。并且，符号 @ 不能作为作为邮箱地址的第一个字符，在 @ 符号之后和点号之前至少要有一个字符：

	<script type="text/javascript">
	<!--
	function validateEmail()
	{
 
	var emailID = document.myForm.EMail.value;
	atpos = emailID.indexOf("@");
	dotpos = emailID.lastIndexOf(".");
	if (atpos < 1 || ( dotpos - atpos < 2 )) 
	{
       alert("Please enter correct email ID")
       document.myForm.EMail.focus() ;
       return false;
	}
	return( true );
	}
	//-->
	</script>

为了更好的理解此处内容，你可以自己[尝试一下](http://www.tutorialspoint.com/cgi-bin/practice.cgi?file=javascript_43)。