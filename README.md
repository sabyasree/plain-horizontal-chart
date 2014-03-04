horizontal chart plain plugin
======================


Here is the code:
============

```
function chart(test, path){
var sum = 0;
for(var i=0; i<test.length; i++)
{
    val= test[i].innerHTML;
    val = val.split(" ");
    val = val[0].replace("S$"," ").split(",").join("").trim();
    sum += parseInt(val);
}
var a =[];
for(var i=0; i<test.length; i++)
{
    val= test[i].innerHTML;
    val = val.split(" ");
    val = val[0].replace("S$"," ").split(",").join("").trim();
    indipercent = (val / sum)*100;
    $(path + " .chart").eq(i).empty().append("<div class='chartview'/>");
    $(path + " .chartview").eq(i).width(0).animate({width: indipercent},"slow");
   
}
}
```

How to use :
============
```
chart(test, path);
```
