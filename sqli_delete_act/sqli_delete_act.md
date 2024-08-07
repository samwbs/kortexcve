***\*A sql injection vulnerability in has been found in SourceCodester Kortex Lite Advocate Office Management System 1.0.(\****delete_act.php***\*)\****

***\*Explaination:\****

SQL injection errors occur when:

Data enters a program from an untrusted source.

The data is used to dynamically construct a SQL query.

***\*Target Code source:\****

https://www.sourcecodester.com/php/17280/advocate-office-management-system-free-download.html

***\*Url:\****  /kortex_lite/control/delete_act.php

***\*Abstract:\****

SQL Injection vulnerability in Kortex Lite Advocate Office Management System v.1.0 allows an attacker to execute arbitrary code via a crafted payload to the id parameter in the delete_act.php component.

***\*Details:\****

In this case the data is passed to query() in delete_act.php at line 8.

 ![1](img/1.png)

 

We can find the delete_act.php interface in View Acts->Action.

![2](img/2.png) 

 sqlmap.py -r delete_act.txt --current-db

![3](img/3.png)

 

GET parameter 'id' is vulnerable.

![4](img/4.png)

![5](img/5.png)