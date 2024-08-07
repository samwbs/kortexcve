***\*A sql injection vulnerability in has been found in SourceCodester Kortex Lite Advocate Office Management System 1.0.(\****activate_act.php***\*)\****

***\*Explaination:\****

SQL injection errors occur when:

Data enters a program from an untrusted source.

The data is used to dynamically construct a SQL query.

***\*Target Code source:\****

https://www.sourcecodester.com/php/17280/advocate-office-management-system-free-download.html

 

***\*Url\****:  kortex_lite/control/activate_act.php

***\*Abstract\****:

SQL Injection vulnerability in Kortex Lite Advocate Office Management System v.1.0 allows an attacker to execute arbitrary code via a crafted payload to the id parameter in the activate_act.php component.

***\*Details:\****

In this case the data is passed to exec() in activate_act.php at line 11.

![1](img/1.png)

 

We can find the activate_act.php interface in View Act->Action(Activate).

![2](img/2.png)



sqlmap.py -r activate_act.txt --current-db

![3](img/3.png)

 

GET parameter 'id' is vulnerable.

![4](img/4.png)

![5](img/5.png)