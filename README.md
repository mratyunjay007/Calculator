# Calculator
upto two decimal digit calculator using javascript

<head>
<title>Two Digit Calculator</title>

<script language="JavaScript">
 var p=0,k='',l='',m='',n='',o='',s=0,a,b,c,dd,e;
function reseter()
{
p=0;}
function writer(x)
{
if(x!=20)
{
p++;

switch(p)
{ case 1: a=x;
          if(a==10)
            {document.f1.d.value='+';
               k='+';}
           else if(a==11)
          {document.f1.d.value="-";
              k='-' }
          else if(a==12)
         {document.f1.d.value="*"; k='*';}
          else if(a==13)
         {document.f1.d.value="/"; k='/';}
          else if(a==0.1)
          {document.f1.d.value="."; k='.';}
         else
          {document.f1.d.value=a; k=a;}
                    break;          

case 2: b=x;
        if(b==10)
          {document.f1.d.value=k+"+";
               l='+';} 
        else if(b==11)
        {document.f1.d.value=k+'-'; l='-';}
        else if(b==12)
         {document.f1.d.value=k+"*"; l='*';}
         else if(b==13)
        {document.f1.d.value=k+"/"; l='/';}
         else if(b==0.1)
        {document.f1.d.value=k+"."; l='.';}
          else
         {document.f1.d.value=k+""+b; l=b;}
         break; 
case 3: c=x;
        if(c==10)
         {document.f1.d.value=k+""+l+'+'; m='+';
         }
        else if(c==11)
          {document.f1.d.value=k+""+l+"-";m='-';}
        else if(c==12)
          {document.f1.d.value=k+""+l+"*";m='*';}
        else if(c==13)
         { document.f1.d.value=k+""+l+"/";m='/';}
         else if(c==0.1)
        {document.f1.d.value=k+""+l+".";m='.';}
         else
        { document.f1.d.value=k+''+l+''+c;m=c;}
         break; 

case 4: dd=x;
        if(dd==10)
         {document.f1.d.value=k+""+l+''+m+'+'; n='+';
         }
        else if(dd==11)
          {document.f1.d.value=k+""+l+""+m+"-";n='-';}
        else if(dd==12)
          {document.f1.d.value=k+""+l+""+m+"*";n='*';}
        else if(dd==13)
         { document.f1.d.value=k+""+l+""+m+"/";n='/';}
         else if(dd==0.1)
        {document.f1.d.value=k+""+l+""+m+".";n='.';}
         else
        { document.f1.d.value=k+''+l+''+m+""+dd;n=dd;}
         break;

case 5: e=x;
        if(e==10)
         {document.f1.d.value=k+''+l+''+m+''+n+'+'; o='+';}
        else if(e==11)
        {document.f1.d.value=k+''+l+''+m+''+n+'-'; o='-';}
          else if(e==12)
         {document.f1.d.value=k+''+l+''+m+''+n+'*';o='*';}
        else if(e==13)
         {document.f1.d.value=k+''+l+''+m+''+n+'/'; o='/';}
        else if(e==0.1)
        {document.f1.d.value=k+''+l+''+m+''+n+'.';o='.';}
        else
        document.f1.d.value=k+''+l+''+m+''+n+''+e; o=e;
         break;

}}
else
{if(p>2)
   { if(p==3)
     {if(a<10 && c<10)
        {if(b>9)
           switch(b)
          {case 10: s=a+c; document.f1.d.value=s; break;
           case 11: s=a-c; document.f1.d.value=s; break;
           case 12: s=a*c; document.f1.d.value=s; break;
           case 13: s=a/c; document.f1.d.value=s; break; 
        
      } } }

  

   if(p==4)
    {if(a<10 && b>9 && c<10 && dd<10 && a!=0.1)
       {cal=c*10+dd;
         
        switch(b)
          {case 10: s=a+cal; document.f1.d.value=s; break;
           case 11: s=a-cal; document.f1.d.value=s; break;
           case 12: s=a*cal; document.f1.d.value=s; break;
           case 13: s=a/cal; document.f1.d.value=s; break; 
         } }
      if(a<10 && b<10 && c>9 && dd<10 && a!=0.1)
         {cal=a*10+b;
          switch(c)
          {case 10: s=cal+dd; document.f1.d.value=s; break;
           case 11: s=cal-dd; document.f1.d.value=s; break;
           case 12: s=cal*dd; document.f1.d.value=s; break;
           case 13: s=cal/dd; document.f1.d.value=s; break; 
      } }
      

  }

 if(p==5)
  {if(a<10 && b>9 && c<10 && dd<10 && e<10 && a!=0.1)
     {
       if(c!=0.1 && dd!=0.1 && e!=0.1)
             { cal=c*100+dd*10+e;}
        else if(c==0.1 && dd!=0.1 && e!=0.1)
             { cal=(dd*10+e)/100;}
         else if( c!=0.1 && dd==0.1 && e!=0.1)
              {cal=(c*10+e)/10;}
         else 
               {cal=c*10+dd;}
       switch(b)
          {case 10: s=a+cal; document.f1.d.value=s; break;
           case 11: s=a-cal; document.f1.d.value=s; break;
           case 12: s=a*cal; document.f1.d.value=s; break;
           case 13: s=a/cal; document.f1.d.value=s; break; 
      }  }

  if(a<10 && b<10 && c>9 && dd<10 && e<10)
    {   if(a!=0.1 && b!=0.1)
          {cal=a*10+b;}
         else if(a==0.1 && b!=0.1)
            {cal=b/10;}
          else if(b==0.1 && a!=0.1)
            {cal=a;}
    
         if(dd==0.1)
          {cal1=e/10;}
          else if(e==0.1 && dd!=0.1)
         {cal1=dd;}
       else
          {cal1=dd*10+e;}
       switch(c)
          {case 10: s=cal+cal1; document.f1.d.value=s; break;
           case 11: s=cal-cal1; document.f1.d.value=s; break;
           case 12: s=cal*cal1; document.f1.d.value=s; break;
           case 13: s=cal/cal1; document.f1.d.value=s; break; 
      } }


  if(a<10 && b<10 && c<10 && dd>9 && e<10 && e!=0.1)
   {       if(a==0.1 && b!=0.1 && c!=0.1)
             {cal=(b*10+c)/100;}
           else if(a!=0.1 && b==0.1 && c!=0.1)
            {cal=(a*10+c)/10;}
          else if(a!=0.1 && b!=0.1 && c==0.1)
            {cal=a*10+b;}
          else
         cal=a*100+b*10+c;
     switch(dd)
          {case 10: s=cal+e; document.f1.d.value=s; break;
           case 11: s=cal-e; document.f1.d.value=s; break;
           case 12: s=cal*e; document.f1.d.value=s; break;
           case 13: s=cal/e; document.f1.d.value=s; break; 
      }
       }
  }

}}}

</script>



</head>

<body bgcolor="#007731" >
<br><br><br><br>
<form name=f1>
<center>
<table cellpadding=2 border=1 bordercolor="#c0c0c0"><tr><td><center> <font  color="#00ffff" >The Javascript Calculator</font></center><br>
<table cellspacing=2 cellpadding=1 border=1 bordercolor="#0000ff" bgcolor="#0f0f00" width=25%>


<tr><td colspan=4><input type="text" name="d" value="It's Me" size="50" maxlength="60"></td></tr>

<tr>
<td bgcolor="#000000" ><input type="button" name="ia" value="7" onclick="writer(7)" style="width:100%"> </td>
<td bgcolor="#000000"><input type=button name=i8 value=8 onclick="writer(8)" style="width:100%"></td> 
<td bgcolor="#000000"><input type=button name=i9 value=9 onclick="writer(9)" style="width:100%"></td>
<td bgcolor="#000000"> <input type=button name=s1 value=/ onclick="writer(13)" style="width:100%"></td></tr>

<tr>
<td bgcolor="#000000"><input type=button name=i4 value=4 onclick=writer(4) style="width:100%" > </td>
<td bgcolor="#000000"><input type=button name=i5 value=5 onclick=writer(5) style="width:100%"></td> 
<td bgcolor="#000000"><input type=button name=i6 value=6 onclick="writer(6)" style="width:100%"></td>
<td bgcolor="#000000"> <input type=button name=s2 value=* onclick="writer(12)" style="width:100%"></td></tr>

<tr>
<td bgcolor="#000000"><input type=button name=i1 value=1 onclick=writer(1) style="width:100%" > </td>
<td bgcolor="#000000"><input type=button name=i2 value=2 onclick="writer(2)" style="width:100%"></td> 
<td bgcolor="#000000"><input type=button name=i3 value=3 onclick="writer(3)" style="width:100%"></td>
<td bgcolor="#000000"> <input type=button name=s3 value=- onclick="writer(11)" style="width:100%"></td></tr>

<tr>
<td bgcolor="#000000" colspan=2><input type=button name=i0 value=0 onclick=writer(0) style="width:100%" > </td>
 
<td bgcolor="#000000"><input type=button name=s5 value=. onclick="writer(0.1)" style="width:100%"></td>
<td bgcolor="#000000"> <input type=button name=s4 value=+ onclick="writer(10)" style="width:100%"></td></tr>

<tr>
<td bgcolor="#000000" colspan=2><input type=button name=s6 value="=" onclick=writer(20) style="width:100%" > </td>
<td bgcolor="#000000" colspan=2> <input type=reset name=s7 value=AC onclick="reseter()" style="width:100%"></td></tr>


</table>
</td></tr></table>
</form>  

<h3 align=right><font color="#ffffff" >Mratyunjay Tripathi</h3>
  </body>
  </html>

