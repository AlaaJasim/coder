# coder

<!DOCTYPE html>
<html>
<head>
<script>

function insert(num){
document.form.textview.value=document.form.textview.value+num;
}
function equal(){
var exp=document.form.textview.value;
if(exp){
document.form.textview.value=eval(exp);
}
}
function clear(){

document.form.textview.value="";
}
function back(){
var exp=document.form.textview.value;
document.form.textview.value=exp.substring(0,exp.length-1);
}

</script>
<style>
.button:hover{
background:linear-gradient(#C6F8FF,#71C2FF,#2681E6,#00BDFF,#6ED0FF);
}
#c:hover{
background:linear-gradient(#C6F8FF,#71C2FF,#2681E6,#00BDFF,#6ED0FF);}
#F:hover{
background:linear-gradient(#C6F8FF,#71C2FF,#2681E6,#00BDFF,#6ED0FF)
;}
#F{
background:black;
color:white;
transition-duration:1s;
}
#c{
background:linear-gradient(#EDEDED,red,#FFB6B9);
color:white;
transition-duration:1s;
}
.button{
padding:0;
border-radius:5px;
width:50px;
height:50px;
font-size:30px;
font-weight:500px;
box-shadow:2px 1px 5px black;
background:linear-gradient(#DDDDDD,#848484,#333333,#595959,#767676);
transition-duration:1s;
color:white;
}
.end:hover{
background:linear-gradient(#C6F8FF,#71C2FF,#2681E6,#00BDFF,#6ED0FF);
}
.end{
width:50px;
height:50px; 
margin-left:60px;
width:160px;
font-size:30px;
border-radius:5px;
box-shadow:2px 1px 5px black;
background:linear-gradient(#00FFF3,#00CEFF,#0083FF,#002CFF);
color:white;
transition-duration:1s;
}
.textview{
width:210px;
margin-left:5px;
margin-top:5px;
border-radius:5px;
padding-top:0;
background:#C2E3E3;
font-size:25px;
}
table{
margin-left:4px;
}
#zero{
height:105px;
position:absolute;
left:15px;
top:225px;
font-size:30px;
}
.main{
border:2px inset black;
background:linear-gradient(#616266,#808080);
box-shadow:2px 1px 5px;
width:225px;
height:345px;
border-radius:10px;
}
.calc{
font-family:serif;
text-align:center;
background:radial-gradient(#FF7900,#F2FF00);
border-radius:50px;
border:solid 1px; 
}
</style>
</head>
<body>
<div class="main">

<form name="form">
<input class="textview" name="textview">
</form>
<table>

<tr>
<td><input type="submit" value="7" class="button" onclick="insert(7)"></td>
<td><input type="submit" value="8" class="button" onclick="insert(8)"></td>
<td><input type="submit" value="9" class="button" onclick="insert(9)"></td>
<td> <input type="submit" value="C" class="button" onclick="back();" id="c"></td>
</tr>
<tr>
<td><input type="submit" value="4" class="button" onclick="insert(4)"></td>
<td><input type="submit" value="5" class="button" onclick="insert(5)"></td>
<td><input type="submit" value="6" class="button" onclick="insert(6)"></td>
<td><input type="submit" value="/" class="button" onclick="insert('/')" id="F"></td>
</tr>
<tr>
<td><input type="submit" value="1" class="button" onclick="insert(1)"></td>
<td><input type="submit" value="2" onclick="insert(2)" class="button"></td>
<td><input type="submit" value="3" class="button" onclick="insert(3)"></td>
<td><input type="submit" value="*" class="button" onclick="insert('*')" id="F"></td>
</tr>
<tr>
<td></td>
<td><input type="submit" value="0" class="button" onclick="insert(0)" ></td>
<td><input type="submit" value="-" class="button" onclick="insert('-')" id="F"></td>
<td><input type="submit" value="+" class="button" onclick="insert('+') "id="F"></td>
</tr>
</table>

<input type="submit" value="=" class="end" onclick="equal()">
<input type="submit" value="." 
class="button" onclick="insert('.')" id="zero">
<p class="calc">Calculater</p> 
</div>
</body>
</html>
