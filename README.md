<!DOCTYPE html>
<html>
<head>
<title>
Calculator Program in JavaScript
</title>

<!-- Begins the JavaScript Code -->
<script>

// Use insert() function to insert the number in textview.
function insert(num) 
{
document.form1.textview.value = document.form1.textview.value + num;
}

// Use equal() function to return the result based on passed values.
function equal()
{
var exp = document.form1.textview.value;
if(exp)
{
document.form1.textview.value = eval(exp)
}
}

/* Here, we create a backspace() function to remove the number at the end of the numeric series in textview. */
function backspace()
{
var exp = document.form1.textview.value;
document.form1.textview.value = exp.substring(0, exp.length - 1); /* remove the element from total length ? 1 */
}


</script>

<!-- Start the coding for CSS -->
<style>
/* Create the Outer layout of the Calculator. */
.formstyle
{
width: 300px;
height: 330px;
margin: 20px auto;
border: 3px solid skyblue;
border-radius: 5px;
padding: 20px;
text-align: center;
background-color: grey;
}

/* Display top horizontal bar that contain some information. */
h1 {
	text-align: center;
	padding: 23px;
	background-color: skyblue;
	color: white;
	}
input:hover
{
background-color: green;
}
	
*{
margin: 0;
padding: 0;
}

/* It is used to create the layout for calculator button. */
.btn{
width: 50px;
height: 50px;
font-size: 25px;
margin: 2px;
cursor: pointer;
background-color: red;
color: white;

}

/* It is used to display the numbers, operations and results. */
.textview{
width: 223px;
margin: 5px;
font-size: 25px;
padding: 5px;
background-color: lightgreen;
}	
	
</style>
</head>
<body>
<h1> Calculator Program in JavaScript </h1>
 <div class= "formstyle">
 <form name = "form1">
 <input class= "textview" name = "textview">
 </form>
 <center>
 <table >
 <tr> 
	<td> <input class = "btn" type = "button" value = "C" onclick = "form1.textview.value = ' ' " > </td>
	<td> <input  class = "btn" type = "button" value = "B" onclick = "backspace()" > </td>
	<td> <input  class = "btn" type = "button" value = "/" onclick = "insert('/')" > </td>
	<td> <input class = "btn" type = "button" value = "x" onclick = "insert('*')" > </td>
	</tr>
	
	 <tr> 
	<td> <input class = "btn" type = "button" value = "7" onclick = "insert(7)" > </td>
	<td> <input class = "btn" type = "button" value = "8" onclick = "insert(8)" > </td>
	<td> <input class = "btn" type = "button" value = "9" onclick = "insert(9)" > </td>
	<td> <input class = "btn" type = "button" value = "-" onclick = "insert('-')" > </td>
	</tr>
	
	 <tr> 
	<td> <input class = "btn" type = "button" value = "4" onclick = "insert(4)" > </td>
	<td> <input class = "btn" type = "button" value = "5" onclick = "insert(5)" > </td>
	<td> <input class = "btn" type = "button" value = "6" onclick = "insert(6)" > </td>
	<td> <input class = "btn" type = "button" value = "+" onclick = "insert('+')" > </td>
	</tr>
	
	 <tr> 
	<td> <input class = "btn" type = "button" value = "1" onclick = "insert(1)" > </td>
	<td> <input class = "btn" type = "button" value = "2" onclick = "insert(2)" > </td>
	<td> <input class = "btn" type = "button" value = "3" onclick = "insert(3)" > </td>
	<td rowspan = 5> <input class = "btn" style = "height: 110px" type = "button" value = "=" onclick = "equal()"> </td>
	</tr>
	<tr>
	<td colspan = 2> <input class = "btn" style = "width: 106px" type = "button" value = "0" onclick = "insert(0)" > </td>
	<td> <input class = "btn" type = "button" value = "." onclick = "insert('.')"> </td>
	</tr>
	</table>
	</center>
 </div>
 </body>
 </html>
