## Stored Procedures

Stored Procedures are pre-compiled objects which are compiled for the first time and its compiled format is saved, which executes (compiled code) whenever it is called. For more about a stored procedure, please refer to the article [Different types of Stored Procedure](http://www.dotnettricks.com/learn/sqlserver/different-types-of-sql-server-stored-procedures).

## Functions

A function is compiled and executed every time whenever it is called. A function must return a value and cannot modify the data received as parameters. For more about functions, please refer to the article [Different types of Functions](http://www.dotnettricks.com/learn/sqlserver/different-types-of-sql-server-functions).



Functions follow the computer-science definition in that they MUST return a value and cannot alter the data they receive as parameters (the arguments). Functions are not allowed to change anything, must have at least one parameter, and they must return a value. Stored procs do not have to have a parameter, can change database objects, and do not have to return a value.

![[Pasted image 20221124130617.png]]

