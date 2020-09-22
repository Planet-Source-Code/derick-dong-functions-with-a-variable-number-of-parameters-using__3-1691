<div align="center">

## Functions with a variable number of parameters using \(\.\.\.\)


</div>

### Description

To demonstrate how to create a function with a variable number of parameters, similar to the printf function. *Just fixed this, so now you can actually read it.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Derick Dong](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/derick-dong.md)
**Level**          |Intermediate
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+
**Category**       |[Documents](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/documents__3-27.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/derick-dong-functions-with-a-variable-number-of-parameters-using__3-1691/archive/master.zip)





### Source Code

<BR>
Somebody asks me how to do something like this,
<BR>
so I'm posting it. Basically, its a function like
<BR>
printf, that can take a variable number of
<BR>
arguments, using the (...). I use something like
<BR>
this to create a string for my graphics programs,
<BR>
and draw the resulting string to the screen.
<BR>
<BR>
// Create a string function
<BR>
void CreateAString(const char *format, ...)
<BR>
{
<BR>
 va_list list;
<BR>
 char string[1024];
<BR>
<BR>
 // Create the string from the parameters
<BR>
 va_start(list, format);
<BR>
 vsprintf((char *)string, format, list);
<BR>
 va_end(list);
<BR>
<BR>
 // Function to draw the string goes here
<BR>
}
<BR>
<BR>
Now, the complete string is stored in 'string'.
<BR>
To use this function, you can use something like:
<BR>
<BR>
void function()
<BR>
{
<BR>
 int num1 = 10, num2 = 20;
<BR>
 CreateAString("NUM1 = %d NUM2 = %d", num1,
        num2);
<BR>
}
<BR>
<BR>
And 'string' would be:
<BR>
<BR>
NUM1 = 10 NUM2 = 20
<BR>
<BR>
Pretty easy. Not used real often, but it can be useful.

