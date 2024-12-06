# Ex03 Time Table
# Date:
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using `<table>` tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM
## views.py:
```
from django.shortcuts import render
from django.http import HttpResponse

# Create your views here.
def index(request):
    return render(request,'ef/index.html')
```

## index.html:
```
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Londrina+Sketch&family=Sixtyfour+Convergence&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="ti.css"/>
    <title>saveetha eng collge</title>
</head>
<style>
    h1{color:rgb(255, 255, 255);
    text-align: center;

}
   table,tr,td,th{
    border: 3PX solid rgb(29, 28, 28);
    border-collapse: collapse;
    font-size: x-large;
    font-weight: bolder;
    font-family: Arial, Helvetica, sans-serif;
    
    

   }
   td{
    text-align: center;
   }
   .WA{
    background-color: rgb(255, 255, 255);
   }
   .PY{
    background-color
    :rgb(255, 255, 255);
   }
   .blackcolour{
    background-color: rgb(252, 252, 252);
}
   .ml{
    background-color: rgb(255, 255, 255);
   }
  .pa{
    background-color: rgb(255, 255, 255);
  }
  th{
    background-color: rgb(235, 235, 235);
  }
  td:hover{
    background-color: transparent;
  }
  .ih{
    width: 100%;
  }
  .cv{
    margin-top: 50px;
    padding: 50%;
    margin-left: 30%;
    margin-right: 40%;
    
  }
 .e{
    text-align: center;
    font-size:xx-large;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
 } 
 .h{
    margin-left: 9%;
 }

</style>
<body>
<div>
    <img src={% static "sec.jpg" %} class="h">
    <hr width="5px">>
</div>    
<div class="e">
SLOT TIMETABLE - PRABANJAN(24900428)
</div>
<table width = '100%'>
  <tr>
        <th>TIME</th>
        <th>MOM</th>
        <th>TUE</th>
        <th>WED</th>
        <th>THRS</th>
        <th>FRI</th>
        <th>SAT</th>
    </tr>
    <tr> 
        <th>8 T0 10</th>
        <td style="background-color: rgb(255, 255, 255);"></td>
        <td style="background-color: rgb(255, 255, 255);"></td>
        <td style="background-color: rgb(255, 255, 255);"></td>
        <td class="ml">INTRO TO ML</td>
        <td class="ml">INTRO TO ML</td>
        <td class="blackcolour">COMM ENG</td>
    </tr>
    <tr>
        <th>10 T0 12</th>
        <td class="PY">PHY FOR QUA</td>
        <td style="background-color: rgb(255, 255, 255);"></td>
        <td class="blackcolour">COMN ENG</td>
        <td class="pa">PY AND MAT</td>
        <td class="WA">FUN OF WA</td>
        <td class="WA">FUN OF WA</td>
    </tr>
    <tr>
        <th>12 TO 1</th>
        <td colspan="6" style="background-color:rgb(252, 242, 242);">LUNCH</td>
    </tr>
    <tr>
        <th>
            1 T0 3
        </th>
        <td class="WA">FUN OF WA</td>
        <td class="pa">PY AND MAT</td>
        <td style="padding: 2px;background-color: rgb(255, 250, 251);">MENTOR</td>
        <td class="PY">PHY FOR QA</td>
        <td class="pa">PY FOE MAT</td>
        <td class="pa">PY MAT MAT</td>
    </tr>
</table> 
<table class="cv">
    <tr>
        <td>S.NO</td>
        <td>SUBJECT CODE</td>
        <TD>SUBJECT NAME</TD>
    </tr>
    <TR>
        <TD>1.</TD>
        <TD>19AI410</TD>
        <TD>INTRODUCTION TO MACHINE LEARNING</TD>
    </TR>
    <TR>
        <TD>2.</TD>
        <TD>19AI414</TD>
        <TD>FUNDAMENTAL OF WEB APPLICATION DEVELOPMENT</TD>
    </TR>
    <TR>
        <TD>3.</TD>
        <TD>19MA220</TD>
        <TD>MATHEMATICS FOE ARTIFICAL INTELLIGENCE</TD>
    </TR>
    <TR>
        <TD>4.</TD>
        <TD>SH3214</TD>
        <TD>PHYSICS FOR QUANTUM</TD>
    </TR>
    <TR>
        <TD>5.</TD>
        <TD>19EN101</TD>
        <TD>COMMUNICATIVE ENGLISH</TD>
    </TR>
</table>

    <li style="order;">
    </li> 
</body>
</div>
</html>
```  
## urls.py:
```
from django.contrib import admin
from django.urls import path
from tab import views
urlpatterns = [
    path('admin/', admin.site.urls),
    path("",views.index,name="index")
]
```
# OUTPUT
![alt text](<Screenshot 2024-12-05 212021.png>)
![alt text](<Screenshot 2024-12-06 082313.png>)
![alt text](<Screenshot 2024-12-06 082422.png>)
# RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
