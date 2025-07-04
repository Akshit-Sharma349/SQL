# SQL
SQL is a Database Language that was developed by IBM in the early 1970's and become available to the public for commercial use in 1979. It is widely accepted as the universal Relatonal Database Management System (RDBMS).
It is generally used by DATA professionals for querying data as it is used to find the relevant information for analysis ,which helps a business in decision making.


There are various commands in SQL that can be broadly divided into 5 categories 
a) DDL
b) DML
c) DQL
d) DCL
e) TCL

FOLLOWING CHART WILL HELP IN UNDERSTANDING THEM IN A BETTER WAY
SQL commands are instructions. It is used to communicate with the database. It is also used to perform specific tasks, functions, and queries of data. SQL can perform various tasks like create a table, add data to tables, drop the table, modify the table, set permission for users. Types of SQL Commands There are five types of SQL commands: DDL, DML, DCL, TCL, and DQL.
1. Data Definition Language (DDL)  DDL changes the structure of the table like creating a table, deleting a table, altering a table, etc. All the command of DDL are auto-committed that means it permanently save all the changes in the database. Here are some commands that come under DDL:
 CREATE, ALTER , DROP , TRUNCATE . CREATE is used to create a new table in the database. Syntax:
1. CREATE TABLE TABLE_NAME (COLUMN_NAME DATATYPES[,....]); Example:
1. CREATE TABLE EMPLOYEE(Name VARCHAR2(20), Email VARCHAR2(100), DOB DATE); b. DROP: It is used to delete both the structure and record stored in the table. Syntax
1. DROP TABLE ; Example
1. DROP TABLE EMPLOYEE; c. ALTER: It is used to alter the structure of the database. This change could be either to modify the characteristics of an existing attribute or probably to add a new attribute. Syntax: To add a new column in the table
1. ALTER TABLE table_name ADD column_name COLUMN-definition; To modify existing column in the table:
1. ALTER TABLE MODIFY(COLUMN DEFINITION....); EXAMPLE
1. ALTER TABLE STU_DETAILS ADD(ADDRESS VARCHAR2(20));
2. ALTER TABLE STU_DETAILS MODIFY (NAME VARCHAR2(20)); d. TRUNCATE: It is used to delete all the rows from the table and free the space containing the table.
Syntax:
1. TRUNCATE TABLE table_name; Example:
1. TRUNCATE TABLE EMPLOYEE; 2. Data Manipulation Language o DML commands are used to modify the database. It is responsible for all form of changes in the database. o The command of DML is not auto-committed that means it can't permanently save all the changes in the database. They can be rollback. Here are some commands that come under DML: o INSERT o UPDATE o DELETE a. INSERT: The INSERT statement is a SQL query. It is used to insert data into the row of a table. Syntax:
1. INSERT INTO TABLE_NAME
2. (col1, col2, col3,.... col N)
3. VALUES (value1, value2, value3, .... valueN); Or
1. INSERT INTO TABLE_NAME
2. VALUES (value1, value2, value3, .... valueN); For example:
1. INSERT INTO javatpoint (Author, Subject) VALUES ("Sonoo", "DBMS"); b. UPDATE: This command is used to update or modify the value of a column in the table. Syntax:
1. UPDATE table_name SET [column_name1= value1,...column_nameN = valueN] [WHERE CONDITION]
For example:
1. UPDATE students
2. SET User_Name = 'AKSHIT'
3. WHERE Student_Id = '3' c. DELETE: It is used to remove one or more row from a table. Syntax:
1. DELETE FROM table_name [WHERE condition]; For example:
1. DELETE FROM javatpoint
2. WHERE Author="AKSHIT"; 3. Data Control Language DCL commands are used to grant and take back authority from any database user. Here are some commands that come under DCL: o Grant o Revoke a. Grant: It is used to give user access privileges to a database. Example
1. GRANT SELECT, UPDATE ON MY_TABLE TO SOME_USER, ANOTHER_USER; b. Revoke: It is used to take back permissions from the user. Example
1. REVOKE SELECT, UPDATE ON MY_TABLE FROM USER1, USER2; 4. Transaction Control Language TCL commands can only use with DML commands like INSERT, DELETE and UPDATE only. These operations are automatically committed in the database that's why they cannot be used while creating tables or dropping them.
Here are some commands that come under TCL: o COMMIT o ROLLBACK o SAVEPOINT a. Commit: Commit command is used to save all the transactions to the database. Syntax:
1. COMMIT; Example:
1. DELETE FROM CUSTOMERS
2. WHERE AGE = 25;
3. COMMIT; b. Rollback: Rollback command is used to undo transactions that have not already been saved to the database. Syntax:
1. ROLLBACK; Example:
1. DELETE FROM CUSTOMERS
2. WHERE AGE = 25;
3. ROLLBACK; c. SAVEPOINT: It is used to roll the transaction back to a certain point without rolling back the entire transaction. Syntax:
1. SAVEPOINT SAVEPOINT_NAME; 5. Data Query Language DQL is used to fetch the data from the database. It uses only one command: o SELECT
a. SELECT: This is the same as the projection operation of relational algebra. It is used to select the attribute based on the condition described by WHERE clause. Syntax:
1. SELECT expressions
2. FROM TABLES
3. WHERE conditions; For example:
1. SELECT emp_name
2. FROM employee
3. WHERE age > 20;
• CREATE TABLE
The SQL CREATE TABLE statement is used to create a new table.
Syntax
The basic syntax of the CREATE TABLE statement is as follows –
CREATE TABLE table_name(
column1 datatype,
column2 datatype,
column3 datatype,
.....
columnN datatype,
PRIMARY KEY( one or more columns )
);
CREATE TABLE Employees_details(
ID int,
Name varchar(20),
Address varchar(20)
);
Ex:
CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL,
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2),
PRIMARY KEY (ID)
); • DROP TABLE
The SQL DROP TABLE statement is used to remove a table definition and all the data, indexes, triggers, constraints and permission specifications for that table.
NOTE − You should be very careful while using this command because once a table is deleted then all the information available in that table will also be lost forever.
Syntax
The basic syntax of this DROP TABLE statement is as follows −
DROP TABLE table_name; • INSERT INTO
The SQL INSERT INTO Statement is used to add new rows of data to a table in the database.
Syntax
There are two basic syntaxes of the INSERT INTO statement which are shown below.
INSERT INTO TABLE_NAME (column1, column2, column3,...columnN)
VALUES (value1, value2, value3,...valueN);
Here, column1, column2, column3,...columnN are the names of the columns in the table into which you want to insert the data.
You may not need to specify the column(s) name in the SQL query if you are adding values for all the columns of the table. But make sure the order of the values is in the same order as the columns in the table.
The SQL INSERT INTO syntax will be as follows −
INSERT INTO TABLE_NAME VALUES (value1,value2,value3,...valueN);
Example
The following statements would create six records in the CUSTOMERS table.
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (1, 'Ramesh', 32, 'Ahmedabad', 2000.00 );
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (2, 'Khilan', 25, 'Delhi', 1500.00 );
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (3, 'kaushik', 23, 'Kota', 2000.00 );
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (4, 'Chaitali', 25, 'Mumbai', 6500.00 );
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (5, 'Hardik', 27, 'Bhopal', 8500.00 );
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (6, 'Komal', 22, 'MP', 4500.00 );
You can create a record in the CUSTOMERS table by using the second syntax as shown below.
INSERT INTO CUSTOMERS
VALUES (7, 'Muffy', 24, 'Indore', 10000.00 );
All the above statements would produce the following records in the CUSTOMERS table as shown below.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
• The Select Query
The SQL SELECT statement is used to fetch the data from a database table which returns this data in the form of a result table. These result tables are called result-sets.
Syntax:
The basic syntax of the SELECT statement is as follows −
SELECT column1, column2, columnN FROM table_name;
Here, column1, column2... are the fields of a table whose values you want to fetch. If you want to fetch all the fields available in the field, then you can use the following syntax.
SELECT * FROM table_name;
Example:
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
The following code is an example, which would fetch the ID, Name and Salary fields of the customers available in CUSTOMERS table.
SQL> SELECT ID, NAME, SALARY FROM CUSTOMERS;
This would produce the following result −
+----+----------+----------+
| ID | NAME | SALARY |
+----+----------+----------+
| 1 | Ramesh | 2000.00 |
| 2 | Khilan | 1500.00 |
| 3 | kaushik | 2000.00 |
| 4 | Chaitali | 6500.00 |
| 5 | Hardik | 8500.00 |
| 6 | Komal | 4500.00 |
| 7 | Muffy | 10000.00 |
+----+----------+----------+
If you want to fetch all the fields of the CUSTOMERS table, then you should use the following query.
SQL> SELECT * FROM CUSTOMERS;
This would produce the result as shown below.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
• WHERE Clause
The SQL WHERE clause is used to specify a condition while fetching the data from a single table or by joining with multiple tables. If the given condition is satisfied, then only it returns a specific value from the table. You should use the WHERE clause to filter the records and fetching only the necessary records.
The WHERE clause is not only used in the SELECT statement, but it is also used in the UPDATE, DELETE statement, etc., which we would examine in the subsequent chapters.
Syntax
The basic syntax of the SELECT statement with the WHERE clause is as shown below.
SELECT column1, column2, columnN
FROM table_name
WHERE [condition]
You can specify a condition using the comparison or logical operators like >, <, =, LIKE, NOT, etc. The following examples would make this concept clear.
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
The following code is an example which would fetch the ID, Name and Salary fields from the CUSTOMERS table, where the salary is greater than 2000 −
SQL> SELECT ID, NAME, SALARY
FROM CUSTOMERS
WHERE SALARY > 2000;
This would produce the following result −
+----+----------+----------+
| ID | NAME | SALARY |
+----+----------+----------+
| 4 | Chaitali | 6500.00 |
| 5 | Hardik | 8500.00 |
| 6 | Komal | 4500.00 |
| 7 | Muffy | 10000.00 |
+----+----------+----------+
The following query is an example, which would fetch the ID, Name and Salary fields from the CUSTOMERS table for a customer with the name Hardik. Here, it is important to note that all the strings should be given inside single quotes (''). Whereas, numeric values should be given without any quote as in the above example.
SQL> SELECT ID, NAME, SALARY
FROM CUSTOMERS
WHERE NAME = 'Hardik';
This would produce the following result −
+----+----------+----------+
| ID | NAME | SALARY |
+----+----------+----------+
| 5 | Hardik | 8500.00 |
+----+----------+----------+
• AND and OR Conjunctive Operators
The SQL AND & OR operators are used to combine multiple conditions to narrow data in an SQL statement. These two operators are called as the conjunctive operators.
These operators provide a means to make multiple comparisons with different operators in the same SQL statement.
▪ The AND Operator
The AND operator allows the existence of multiple conditions in an SQL statement's WHERE clause.
Syntax
The basic syntax of the AND operator with a WHERE clause is as follows −
SELECT column1, column2, columnN
FROM table_name
WHERE [condition1] AND [condition2]...AND [conditionN];
You can combine N number of conditions using the AND operator. For an action to be taken by the SQL statement, whether it be a transaction or a query, all conditions separated by the AND must be TRUE.
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Following is an example, which would fetch the ID, Name and Salary fields from the CUSTOMERS table, where the salary is greater than 2000 and the age is less than 25 years −
SQL> SELECT ID, NAME, SALARY
FROM CUSTOMERS
WHERE SALARY > 2000 AND age < 25;
This would produce the following result −
+----+-------+----------+
| ID | NAME | SALARY |
+----+-------+----------+
| 6 | Komal | 4500.00 |
| 7 | Muffy | 10000.00 |
+----+-------+----------+
▪ The OR Operator
The OR operator is used to combine multiple conditions in an SQL statement's WHERE clause.
Syntax
The basic syntax of the OR operator with a WHERE clause is as follows −
SELECT column1, column2, columnN
FROM table_name
WHERE [condition1] OR [condition2]...OR [conditionN]
You can combine N number of conditions using the OR operator. For an action to be taken by the SQL statement, whether it be a transaction or query, the only any ONE of the conditions separated by the OR must be TRUE.
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
The following code block hasa query, which would fetch the ID, Name and Salary fields from the CUSTOMERS table, where the salary is greater than 2000 OR the age is less than 25 years.
SQL> SELECT ID, NAME, SALARY
FROM CUSTOMERS
WHERE SALARY > 2000 OR age < 25;
This would produce the following result −
+----+----------+----------+
| ID | NAME | SALARY |
+----+----------+----------+
| 3 | kaushik | 2000.00 |
| 4 | Chaitali | 6500.00 |
| 5 | Hardik | 8500.00 |
| 6 | Komal | 4500.00 |
| 7 | Muffy | 10000.00 |
• UPDATE Query
The SQL UPDATE Query is used to modify the existing records in a table. You can use the WHERE clause with the UPDATE query to update the selected rows, otherwise all the rows would be affected.
Syntax
The basic syntax of the UPDATE query with a WHERE clause is as follows −
UPDATE table_name
SET column1 = value1, column2 = value2...., columnN = valueN
WHERE [condition];
You can combine N number of conditions using the AND or the OR operators.
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
The following query will update the ADDRESS for a customer whose ID number is 6 in the table.
SQL> UPDATE CUSTOMERS
SET ADDRESS = 'Pune'
WHERE ID = 6;
Now, the CUSTOMERS table would have the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | Pune | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
If you want to modify all the ADDRESS and the SALARY column values in the CUSTOMERS table, you do not need to use the WHERE clause as the UPDATE query would be enough as shown in the following code block.
SQL> UPDATE CUSTOMERS
SET ADDRESS = 'Pune', SALARY = 1000.00;
Now, CUSTOMERS table would have the following records −
+----+----------+-----+---------+---------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+---------+---------+
| 1 | Ramesh | 32 | Pune | 1000.00 |
| 2 | Khilan | 25 | Pune | 1000.00 |
| 3 | kaushik | 23 | Pune | 1000.00 |
| 4 | Chaitali | 25 | Pune | 1000.00 |
| 5 | Hardik | 27 | Pune | 1000.00 |
| 6 | Komal | 22 | Pune | 1000.00 |
| 7 | Muffy | 24 | Pune | 1000.00 |
+----+----------+-----+---------+---------+
• DELETE Query
The SQL DELETE Query is used to delete the existing records from a table.
You can use the WHERE clause with a DELETE query to delete the selected rows, otherwise all the records would be deleted.
Syntax
The basic syntax of the DELETE query with the WHERE clause is as follows −
DELETE FROM table_name
WHERE [condition];
You can combine N number of conditions using AND or OR operators.
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
The following code has a query, which will DELETE a customer, whose ID is 6.
SQL> DELETE FROM CUSTOMERS
WHERE ID = 6;
Now, the CUSTOMERS table would have the following records.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
If you want to DELETE all the records from the CUSTOMERS table, you do not need to use the WHERE clause and the DELETE query would be as follows −
SQL> DELETE FROM CUSTOMERS;
Now, the CUSTOMERS table would not have any record.
• LIKE Clause
The SQL LIKE clause is used to compare a value to similar values using wildcard operators. There are two wildcards used in conjunction with the LIKE operator.
• The percent sign (%)
• The underscore (_)
The percent sign represents zero, one or multiple characters. The underscore represents a single number or character. These symbols can be used in combinations.
Syntax
The basic syntax of % and _ is as follows −
SELECT FROM table_name
WHERE column LIKE 'XXXX%'
or
SELECT FROM table_name
WHERE column LIKE '%XXXX%'
or
SELECT FROM table_name
WHERE column LIKE 'XXXX_'
or
SELECT FROM table_name
WHERE column LIKE '_XXXX'
or
SELECT FROM table_name
WHERE column LIKE '_XXXX_'
You can combine N number of conditions using AND or OR operators. Here, XXXX could be any numeric or string value.
Example
The following table has a few examples showing the WHERE part having different LIKE clause with '%' and '_' operators − Sr.No. Statement & Description
1
WHERE SALARY LIKE '200%'
Finds any values that start with 200.
2
WHERE SALARY LIKE '%200%'
Finds any values that have 200 in any position.
3
WHERE SALARY LIKE '_00%'
Finds any values that have 00 in the second and third positions.
4
WHERE SALARY LIKE '2_%_%'
Finds any values that start with 2 and are at least 3 characters in length.
5
WHERE SALARY LIKE '%2'
Finds any values that end with 2.
6
WHERE SALARY LIKE '_2%3'
Finds any values that have a 2 in the second position and end with a 3.
7
WHERE SALARY LIKE '2___3'
Finds any values in a five-digit number that start with 2 and end with 3.
Let us take a real example, consider the CUSTOMERS table having the records as shown below.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Following is an example, which would display all the records from the CUSTOMERS table, where the SALARY starts with 200.
SQL> SELECT * FROM CUSTOMERS
WHERE SALARY LIKE '200%';
This would produce the following result −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
+----+----------+-----+-----------+----------+
• WILDCARD Operator
The SQL LIKE operator, which is used to compare a value to similar values using the wildcard operators.
SQL supports two wildcard operators in conjunction with the LIKE operator which are explained in detail in the following table. Sr.No. Wildcard & Description
1
The percent sign (%)
Matches one or more characters.
Note − MS Access uses the asterisk (*) wildcard character instead of the percent sign (%) wildcard character.
2
The underscore (_)
Matches one character.
Note − MS Access uses a question mark (?) instead of the underscore (_) to match any one character.
The percent sign represents zero, one or multiple characters. The underscore represents a single number or a character. These symbols can be used in combinations.
Syntax
The basic syntax of a '%' and a '_' operator is as follows.
SELECT * FROM table_name
WHERE column LIKE 'XXXX%'
or
SELECT * FROM table_name
WHERE column LIKE '%XXXX%'
or
SELECT * FROM table_name
WHERE column LIKE 'XXXX_'
or
SELECT * FROM table_name
WHERE column LIKE '_XXXX'
or
SELECT * FROM table_name
WHERE column LIKE '_XXXX_'
You can combine N number of conditions using the AND or the OR operators. Here, XXXX could be any numeric or string value.
Example
The following table has a number of examples showing the WHERE part having different LIKE clauses with '%' and '_' operators. Sr.No. Statement & Description
1
WHERE SALARY LIKE '200%'
Finds any values that start with 200.
2
WHERE SALARY LIKE '%200%'
Finds any values that have 200 in any position.
3
WHERE SALARY LIKE '_00%'
Finds any values that have 00 in the second and third positions.
4
WHERE SALARY LIKE '2_%_%'
Finds any values that start with 2 and are at least 3 characters in length.
5
WHERE SALARY LIKE '%2'
Finds any values that end with 2.
6
WHERE SALARY LIKE '_2%3'
Finds any values that have a 2 in the second position and end with a 3.
7
WHERE SALARY LIKE '2___3'
Finds any values in a five-digit number that start with 2 and end with 3.
Let us take a real example, consider the CUSTOMERS table having the following records.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
The following code block is an example, which would display all the records from the CUSTOMERS table where the SALARY starts with 200.
SQL> SELECT * FROM CUSTOMERS
WHERE SALARY LIKE '200%';
This would produce the following result.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
+----+----------+-----+-----------+----------+
• TOP, LIMIT or ROWNUM Clause
The SQL TOP clause is used to fetch a TOP N number or X percent records from a table.
Note − All the databases do not support the TOP clause. For example MySQL supports the LIMIT clause to fetch limited number of records while Oracle uses the ROWNUM command to fetch a limited number of records.
Syntax
The basic syntax of the TOP clause with a SELECT statement would be as follows.
SELECT TOP number|percent column_name(s)
FROM table_name
WHERE [condition]
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
The following query is an example on the SQL server, which would fetch the top 3 records from the CUSTOMERS table.
SQL> SELECT TOP 3 * FROM CUSTOMERS;
This would produce the following result −
+----+---------+-----+-----------+---------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+---------+-----+-----------+---------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
+----+---------+-----+-----------+---------+
If you are using MySQL server, then here is an equivalent example −
SQL> SELECT * FROM CUSTOMERS
LIMIT 3;
This would produce the following result −
+----+---------+-----+-----------+---------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+---------+-----+-----------+---------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
+----+---------+-----+-----------+---------+
If you are using an Oracle server, then the following code block has an equivalent example.
SQL> SELECT * FROM CUSTOMERS
WHERE ROWNUM <= 3;
This would produce the following result −
+----+---------+-----+-----------+---------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+---------+-----+-----------+---------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
+----+---------+-----+-----------+---------+
• ORDER BY Clause
The SQL ORDER BY clause is used to sort the data in ascending or descending order, based on one or more columns. Some databases sort the query results in an ascending order by default.
Syntax
The basic syntax of the ORDER BY clause is as follows −
SELECT column-list
FROM table_name
[WHERE condition]
[ORDER BY column1, column2, .. columnN] [ASC | DESC];
You can use more than one column in the ORDER BY clause. Make sure whatever column you are using to sort that column should be in the column-list.
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
The following code block has an example, which would sort the result in an ascending order by the NAME and the SALARY −
SQL> SELECT * FROM CUSTOMERS
ORDER BY NAME, SALARY;
This would produce the following result −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
+----+----------+-----+-----------+----------+
The following code block has an example, which would sort the result in the descending order by NAME.
SQL> SELECT * FROM CUSTOMERS
ORDER BY NAME DESC;
This would produce the following result −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
+----+----------+-----+-----------+----------+
• Group By Clause
The SQL GROUP BY clause is used in collaboration with the SELECT statement to arrange identical data into groups. This GROUP BY clause follows the WHERE clause in a SELECT statement and precedes the ORDER BY clause.
Syntax
The basic syntax of a GROUP BY clause is shown in the following code block. The GROUP BY clause must follow the conditions in the WHERE clause and must precede the ORDER BY clause if one is used.
SELECT column1, column2
FROM table_name
WHERE [ conditions ]
GROUP BY column1, column2
ORDER BY column1, column2
Example
Consider the CUSTOMERS table is having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
If you want to know the total amount of the salary on each customer, then the GROUP BY query would be as follows.
SQL> SELECT NAME, SUM(SALARY) FROM CUSTOMERS
GROUP BY NAME;
This would produce the following result −
+----------+-------------+
| NAME | SUM(SALARY) |
+----------+-------------+
| Chaitali | 6500.00 |
| Hardik | 8500.00 |
| kaushik | 2000.00 |
| Khilan | 1500.00 |
| Komal | 4500.00 |
| Muffy | 10000.00 |
| Ramesh | 2000.00 |
+----------+-------------+
Now, let us look at a table where the CUSTOMERS table has the following records with duplicate names −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Ramesh | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | kaushik | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Now again, if you want to know the total amount of salary on each customer, then the GROUP BY query would be as follows −
SQL> SELECT NAME, SUM(SALARY) FROM CUSTOMERS
GROUP BY NAME;
This would produce the following result −
+---------+-------------+
| NAME | SUM(SALARY) |
+---------+-------------+
| Hardik | 8500.00 |
| kaushik | 8500.00 |
| Komal | 4500.00 |
| Muffy | 10000.00 |
| Ramesh | 3500.00 |
+---------+-------------+
• Distinct Keyword
The SQL DISTINCT keyword is used in conjunction with the SELECT statement to eliminate all the duplicate records and fetching only unique records.
There may be a situation when you have multiple duplicate records in a table. While fetching such records, it makes more sense to fetch only those unique records instead of fetching duplicate records.
Syntax
The basic syntax of DISTINCT keyword to eliminate the duplicate records is as follows −
SELECT DISTINCT column1, column2,.....columnN
FROM table_name
WHERE [condition]
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
First, let us see how the following SELECT query returns the duplicate salary records.
SQL> SELECT SALARY FROM CUSTOMERS
ORDER BY SALARY;
This would produce the following result, where the salary (2000) is coming twice which is a duplicate record from the original table.
+----------+
| SALARY |
+----------+
| 1500.00 |
| 2000.00 |
| 2000.00 |
| 4500.00 |
| 6500.00 |
| 8500.00 |
| 10000.00 |
+----------+
Now, let us use the DISTINCT keyword with the above SELECT query and then see the result.
SQL> SELECT DISTINCT SALARY FROM CUSTOMERS
ORDER BY SALARY;
This would produce the following result where we do not have any duplicate entry.
+----------+
| SALARY |
+----------+
| 1500.00 |
| 2000.00 |
| 4500.00 |
| 6500.00 |
| 8500.00 |
| 10000.00 |
+----------+
• Alias query
You can rename a table or a column temporarily by giving another name known as Alias. The use of table aliases is to rename a table in a specific SQL statement. The renaming is a temporary change and the actual table name does not change in the database. The column aliases are used to rename a table's columns for the purpose of a particular SQL query.
Syntax
The basic syntax of a table alias is as follows.
SELECT column1, column2....
FROM table_name AS alias_name
WHERE [condition];
The basic syntax of a column alias is as follows.
SELECT column_name AS alias_name
FROM table_name
WHERE [condition];
Example
Consider the following two tables.
Table 1 − CUSTOMERS Table is as follows.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Table 2 − ORDERS Table is as follows.
+-----+---------------------+-------------+--------+
|OID | DATE | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 | 3 | 3000 |
| 100 | 2009-10-08 00:00:00 | 3 | 1500 |
| 101 | 2009-11-20 00:00:00 | 2 | 1560 |
| 103 | 2008-05-20 00:00:00 | 4 | 2060 |
+-----+---------------------+-------------+--------+
Now, the following code block shows the usage of a table alias.
SQL> SELECT C.ID, C.NAME, C.AGE, O.AMOUNT
FROM CUSTOMERS AS C, ORDERS AS O
WHERE C.ID = O.CUSTOMER_ID;
This would produce the following result.
+----+----------+-----+--------+
| ID | NAME | AGE | AMOUNT |
+----+----------+-----+--------+
| 3 | kaushik | 23 | 3000 |
| 3 | kaushik | 23 | 1500 |
| 2 | Khilan | 25 | 1560 |
| 4 | Chaitali | 25 | 2060 |
+----+----------+-----+--------+
Following is the usage of a column alias.
SQL> SELECT ID AS CUSTOMER_ID, NAME AS CUSTOMER_NAME
FROM CUSTOMERS
WHERE SALARY IS NOT NULL;
This would produce the following result.
+-------------+---------------+
| CUSTOMER_ID | CUSTOMER_NAME |
+-------------+---------------+
| 1 | Ramesh |
| 2 | Khilan |
| 3 | kaushik |
| 4 | Chaitali |
| 5 | Hardik |
| 6 | Komal |
| 7 | Muffy |
+-------------+---------------+
• UNIONS CLAUSE
The SQL UNION clause/operator is used to combine the results of two or more SELECT statements without returning any duplicate rows.
To use this UNION clause, each SELECT statement must have
• The same number of columns selected
• The same number of column expressions
• The same data type and
• Have them in the same order
But they need not have to be in the same length.
Syntax
The basic syntax of a UNION clause is as follows −
SELECT column1 [, column2 ]
FROM table1 [, table2 ]
[WHERE condition]
UNION
SELECT column1 [, column2 ]
FROM table1 [, table2 ]
[WHERE condition]
Here, the given condition could be any given expression based on your requirement.
Example
Consider the following two tables.
Table 1 − CUSTOMERS Table is as follows.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Table 2 − ORDERS Table is as follows.
+-----+---------------------+-------------+--------+
|OID | DATE | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 | 3 | 3000 |
| 100 | 2009-10-08 00:00:00 | 3 | 1500 |
| 101 | 2009-11-20 00:00:00 | 2 | 1560 |
| 103 | 2008-05-20 00:00:00 | 4 | 2060 |
+-----+---------------------+-------------+--------+
Now, let us join these two tables in our SELECT statement as follows −
SQL> SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
LEFT JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID
UNION
SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
RIGHT JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
This would produce the following result −
+------+----------+--------+---------------------+
| ID | NAME | AMOUNT | DATE |
+------+----------+--------+---------------------+
| 1 | Ramesh | NULL | NULL |
| 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
| 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
| 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
| 5 | Hardik | NULL | NULL |
| 6 | Komal | NULL | NULL |
| 7 | Muffy | NULL | NULL |
+------+----------+--------+---------------------+
• The UNION ALL Clause
The UNION ALL operator is used to combine the results of two SELECT statements including duplicate rows.
The same rules that apply to the UNION clause will apply to the UNION ALL operator.
Syntax
The basic syntax of the UNION ALL is as follows.
SELECT column1 [, column2 ]
FROM table1 [, table2 ]
[WHERE condition]
UNION ALL
SELECT column1 [, column2 ]
FROM table1 [, table2 ]
[WHERE condition]
Here, the given condition could be any given expression based on your requirement.
Example
Consider the following two tables,
Table 1 − CUSTOMERS Table is as follows.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Table 2 − ORDERS table is as follows.
+-----+---------------------+-------------+--------+
|OID | DATE | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 | 3 | 3000 |
| 100 | 2009-10-08 00:00:00 | 3 | 1500 |
| 101 | 2009-11-20 00:00:00 | 2 | 1560 |
| 103 | 2008-05-20 00:00:00 | 4 | 2060 |
+-----+---------------------+-------------+--------+
Now, let us join these two tables in our SELECT statement as follows −
SQL> SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
LEFT JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID
UNION ALL
SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
RIGHT JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
This would produce the following result −
+------+----------+--------+---------------------+
| ID | NAME | AMOUNT | DATE |
+------+----------+--------+---------------------+
| 1 | Ramesh | NULL | NULL |
| 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
| 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
| 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
| 5 | Hardik | NULL | NULL |
| 6 | Komal | NULL | NULL |
| 7 | Muffy | NULL | NULL |
| 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
| 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
| 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
+------+----------+--------+---------------------+
There are two other clauses (i.e., operators), which are like the UNION clause.
• SQL INTERSECT Clause − This is used to combine two SELECT statements, but returns rows only from the first SELECT statement that are identical to a row in the second SELECT statement.
• SQL EXCEPT Clause − This combines two SELECT statements and returns rows from the first SELECT statement that are not returned by the second SELECT statement.
• Using Joins
The SQL Joins clause is used to combine records from two or more tables in a database. A JOIN is a means for combining fields from two tables by using values common to each.
Consider the following two tables −
Table 1 − CUSTOMERS Table
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Table 2 − ORDERS Table
+-----+---------------------+-------------+--------+
|OID | DATE | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 | 3 | 3000 |
| 100 | 2009-10-08 00:00:00 | 3 | 1500 |
| 101 | 2009-11-20 00:00:00 | 2 | 1560 |
| 103 | 2008-05-20 00:00:00 | 4 | 2060 |
+-----+---------------------+-------------+--------+
Now, let us join these two tables in our SELECT statement as shown below.
SQL> SELECT ID, NAME, AGE, AMOUNT
FROM CUSTOMERS, ORDERS
WHERE CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
This would produce the following result.
+----+----------+-----+--------+
| ID | NAME | AGE | AMOUNT |
+----+----------+-----+--------+
| 3 | kaushik | 23 | 3000 |
| 3 | kaushik | 23 | 1500 |
| 2 | Khilan | 25 | 1560 |
| 4 | Chaitali | 25 | 2060 |
+----+----------+-----+--------+
Here, it is noticeable that the join is performed in the WHERE clause. Several operators can be used to join tables, such as =, <, >, <>, <=, >=, !=, BETWEEN, LIKE, and NOT; they can all be used to join tables. However, the most common operator is the equal to symbol.
There are different types of joins available in SQL −
• INNER JOIN − returns rows when there is a match in both tables.
• LEFT JOIN − returns all rows from the left table, even if there are no matches in the right table.
• RIGHT JOIN − returns all rows from the right table, even if there are no matches in the left table.
•
• FULL JOIN − returns rows when there is a match in one of the tables.
• SELF JOIN − is used to join a table to itself as if the table were two tables, temporarily renaming at least one table in the SQL statement.
• CARTESIAN JOIN − returns the Cartesian product of the sets of records from the two or more joined tables.
1. INNER JOIN
• The most important and frequently used of the joins is the INNER JOIN. They are also referred to as an EQUIJOIN.
• The INNER JOIN creates a new result table by combining column values of two tables (table1 and table2) based upon the join-predicate. The query compares each row of table1 with each row of table2 to find all pairs of rows which satisfy the join-predicate. When the join-predicate is satisfied, column values for each matched pair of rows of A and B are combined into a result row.
• Syntax
• The basic syntax of the INNER JOIN is as follows.
• SELECT table1.column1, table1.column2,table2.column2...
• FROM table1
• INNER JOIN table2
• ON table1.common_field = table2.common_field;
• Example
• Consider the following two tables.
• Table 1 − CUSTOMERS Table is as follows.
• +----+----------+-----+-----------+----------+
• | ID | NAME | AGE | ADDRESS | SALARY |
• +----+----------+-----+-----------+----------+
• | 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
• | 2 | Khilan | 25 | Delhi | 1500.00 |
• | 3 | kaushik | 23 | Kota | 2000.00 |
• | 4 | Chaitali | 25 | Mumbai | 6500.00 |
• | 5 | Hardik | 27 | Bhopal | 8500.00 |
• | 6 | Komal | 22 | MP | 4500.00 |
• | 7 | Muffy | 24 | Indore | 10000.00 |
• +----+----------+-----+-----------+----------+
• Table 2 − ORDERS Table is as follows.
• +-----+---------------------+-------------+--------+
• | OID | DATE | CUSTOMER_ID | AMOUNT |
• +-----+---------------------+-------------+--------+
• | 102 | 2009-10-08 00:00:00 | 3 | 3000 |
• | 100 | 2009-10-08 00:00:00 | 3 | 1500 |
• | 101 | 2009-11-20 00:00:00 | 2 | 1560 |
• | 103 | 2008-05-20 00:00:00 | 4 | 2060 |
• +-----+---------------------+-------------+--------+
• Now, let us join these two tables using the INNER JOIN as follows −
• SQL> SELECT ID, NAME, AMOUNT, DATE
• FROM CUSTOMERS
• INNER JOIN ORDERS
• ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
• This would produce the following result.
• +----+----------+--------+---------------------+
• | ID | NAME | AMOUNT | DATE |
• +----+----------+--------+---------------------+
• | 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
• | 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
• | 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
• | 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
• +----+----------+--------+---------------------+
2. LEFT JOIN
The SQL LEFT JOIN returns all rows from the left table, even if there are no matches in the right table. This means that if the ON clause matches 0 (zero) records in the right table; the join will still return a row in the result, but with NULL in each column from the right table.
This means that a left join returns all the values from the left table, plus matched values from the right table or NULL in case of no matching join predicate.
Syntax
The basic syntax of a LEFT JOIN is as follows.
SELECT table1.column1, table2.column2...
FROM table1
LEFT JOIN table2
ON table1.common_field = table2.common_field;
Here, the given condition could be any given expression based on your requirement.
Example
Consider the following two tables,
Table 1 − CUSTOMERS Table is as follows.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Table 2 − Orders Table is as follows.
+-----+---------------------+-------------+--------+
| OID | DATE | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 | 3 | 3000 |
| 100 | 2009-10-08 00:00:00 | 3 | 1500 |
| 101 | 2009-11-20 00:00:00 | 2 | 1560 |
| 103 | 2008-05-20 00:00:00 | 4 | 2060 |
+-----+---------------------+-------------+--------+
Now, let us join these two tables using the LEFT JOIN as follows.
SQL> SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
LEFT JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
This would produce the following result −
+----+----------+--------+---------------------+
| ID | NAME | AMOUNT | DATE |
+----+----------+--------+---------------------+
| 1 | Ramesh | NULL | NULL |
| 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
| 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
| 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
| 5 | Hardik | NULL | NULL |
| 6 | Komal | NULL | NULL |
| 7 | Muffy | NULL | NULL |
+----+----------+--------+---------------------+
3.RIGHT JOIN
The SQL RIGHT JOIN returns all rows from the right table, even if there are no matches in the left table. This means that if the ON clause matches 0 (zero) records in the left table; the join will still return a row in the result, but with NULL in each column from the left table.
This means that a right join returns all the values from the right table, plus matched values from the left table or NULL in case of no matching join predicate.
Syntax
The basic syntax of a RIGHT JOIN is as follow.
SELECT table1.column1, table2.column2...
FROM table1
RIGHT JOIN table2
ON table1.common_field = table2.common_field;
Example
Consider the following two tables,
Table 1 − CUSTOMERS Table is as follows.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Table 2 − ORDERS Table is as follows.
+-----+---------------------+-------------+--------+
|OID | DATE | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 | 3 | 3000 |
| 100 | 2009-10-08 00:00:00 | 3 | 1500 |
| 101 | 2009-11-20 00:00:00 | 2 | 1560 |
| 103 | 2008-05-20 00:00:00 | 4 | 2060 |
+-----+---------------------+-------------+--------+
Now, let us join these two tables using the RIGHT JOIN as follows.
SQL> SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
RIGHT JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
This would produce the following result −
+------+----------+--------+---------------------+
| ID | NAME | AMOUNT | DATE |
+------+----------+--------+---------------------+
| 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
| 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
| 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
+------+----------+--------+---------------------+
4.FULL JOIN
The SQL FULL JOIN combines the results of both left and right outer joins.
The joined table will contain all records from both the tables and fill in NULLs for missing matches on either side.
Syntax
The basic syntax of a FULL JOIN is as follows −
SELECT table1.column1, table2.column2...
FROM table1
FULL JOIN table2
ON table1.common_field = table2.common_field;
Here, the given condition could be any given expression based on your requirement.
Example
Consider the following two tables.
Table 1 − CUSTOMERS Table is as follows.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Table 2 − ORDERS Table is as follows.
+-----+---------------------+-------------+--------+
|OID | DATE | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 | 3 | 3000 |
| 100 | 2009-10-08 00:00:00 | 3 | 1500 |
| 101 | 2009-11-20 00:00:00 | 2 | 1560 |
| 103 | 2008-05-20 00:00:00 | 4 | 2060 |
+-----+---------------------+-------------+--------+
Now, let us join these two tables using FULL JOIN as follows.
SQL> SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
FULL JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
This would produce the following result −
+------+----------+--------+---------------------+
| ID | NAME | AMOUNT | DATE |
+------+----------+--------+---------------------+
| 1 | Ramesh | NULL | NULL |
| 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
| 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
| 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
| 5 | Hardik | NULL | NULL |
| 6 | Komal | NULL | NULL |
| 7 | Muffy | NULL | NULL |
| 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
| 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
| 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
+------+----------+--------+---------------------+
If your Database does not support FULL JOIN (MySQL does not support FULL JOIN), then you can use UNION ALL clause to combine these two JOINS as shown below.
SQL> SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
LEFT JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID
UNION ALL
SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS
RIGHT JOIN ORDERS
ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID
5.SELF JOINS
The SQL SELF JOIN is used to join a table to itself as if the table were two tables; temporarily renaming at least one table in the SQL statement.
Syntax
The basic syntax of SELF JOIN is as follows −
SELECT a.column_name, b.column_name...
FROM table1 a, table1 b
WHERE a.common_field = b.common_field;
Here, the WHERE clause could be any given expression based on your requirement.
Example
Consider the following table.
CUSTOMERS Table is as follows.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Now, let us join this table using SELF JOIN as follows −
SQL> SELECT a.ID, b.NAME, a.SALARY
FROM CUSTOMERS a, CUSTOMERS b
WHERE a.SALARY < b.SALARY;
This would produce the following result −
+----+----------+---------+
| ID | NAME | SALARY |
+----+----------+---------+
| 2 | Ramesh | 1500.00 |
| 2 | kaushik | 1500.00 |
| 1 | Chaitali | 2000.00 |
| 2 | Chaitali | 1500.00 |
| 3 | Chaitali | 2000.00 |
| 6 | Chaitali | 4500.00 |
| 1 | Hardik | 2000.00 |
| 2 | Hardik | 1500.00 |
| 3 | Hardik | 2000.00 |
| 4 | Hardik | 6500.00 |
| 6 | Hardik | 4500.00 |
| 1 | Komal | 2000.00 |
| 2 | Komal | 1500.00 |
| 3 | Komal | 2000.00 |
| 1 | Muffy | 2000.00 |
| 2 | Muffy | 1500.00 |
| 3 | Muffy | 2000.00 |
| 4 | Muffy | 6500.00 |
| 5 | Muffy | 8500.00 |
| 6 | Muffy | 4500.00 |
+----+----------+---------+
6. CARTESIAN JOIN
The CARTESIAN JOIN or CROSS JOIN returns the Cartesian product of the sets of records from two or more joined tables. Thus, it equates to an inner join where the join-condition always evaluates to either True or where the join-condition is absent from the statement.
Syntax
The basic syntax of the CARTESIAN JOIN or the CROSS JOIN is as follows −
SELECT table1.column1, table2.column2...
FROM table1, table2 [, table3 ]
Example
Consider the following two tables.
Table 1 − CUSTOMERS table is as follows.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Table 2: ORDERS Table is as follows −
+-----+---------------------+-------------+--------+
|OID | DATE | CUSTOMER_ID | AMOUNT |
+-----+---------------------+-------------+--------+
| 102 | 2009-10-08 00:00:00 | 3 | 3000 |
| 100 | 2009-10-08 00:00:00 | 3 | 1500 |
| 101 | 2009-11-20 00:00:00 | 2 | 1560 |
| 103 | 2008-05-20 00:00:00 | 4 | 2060 |
+-----+---------------------+-------------+--------+
Now, let us join these two tables using CARTESIAN JOIN as follows −
SQL> SELECT ID, NAME, AMOUNT, DATE
FROM CUSTOMERS, ORDERS;
This would produce the following result −
+----+----------+--------+---------------------+
| ID | NAME | AMOUNT | DATE |
+----+----------+--------+---------------------+
| 1 | Ramesh | 3000 | 2009-10-08 00:00:00 |
| 1 | Ramesh | 1500 | 2009-10-08 00:00:00 |
| 1 | Ramesh | 1560 | 2009-11-20 00:00:00 |
| 1 | Ramesh | 2060 | 2008-05-20 00:00:00 |
| 2 | Khilan | 3000 | 2009-10-08 00:00:00 |
| 2 | Khilan | 1500 | 2009-10-08 00:00:00 |
| 2 | Khilan | 1560 | 2009-11-20 00:00:00 |
| 2 | Khilan | 2060 | 2008-05-20 00:00:00 |
| 3 | kaushik | 3000 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1500 | 2009-10-08 00:00:00 |
| 3 | kaushik | 1560 | 2009-11-20 00:00:00 |
| 3 | kaushik | 2060 | 2008-05-20 00:00:00 |
| 4 | Chaitali | 3000 | 2009-10-08 00:00:00 |
| 4 | Chaitali | 1500 | 2009-10-08 00:00:00 |
| 4 | Chaitali | 1560 | 2009-11-20 00:00:00 |
| 4 | Chaitali | 2060 | 2008-05-20 00:00:00 |
| 5 | Hardik | 3000 | 2009-10-08 00:00:00 |
| 5 | Hardik | 1500 | 2009-10-08 00:00:00 |
| 5 | Hardik | 1560 | 2009-11-20 00:00:00 |
| 5 | Hardik | 2060 | 2008-05-20 00:00:00 |
| 6 | Komal | 3000 | 2009-10-08 00:00:00 |
| 6 | Komal | 1500 | 2009-10-08 00:00:00 |
| 6 | Komal | 1560 | 2009-11-20 00:00:00 |
| 6 | Komal | 2060 | 2008-05-20 00:00:00 |
| 7 | Muffy | 3000 | 2009-10-08 00:00:00 |
| 7 | Muffy | 1500 | 2009-10-08 00:00:00 |
| 7 | Muffy | 1560 | 2009-11-20 00:00:00 |
| 7 | Muffy | 2060 | 2008-05-20 00:00:00 |
+----+----------+--------+---------------------+
• Constraints
Constraints are the rules enforced on the data columns of a table. These are used to limit the type of data that can go into a table. This ensures the accuracy and reliability of the data in the database.
Constraints could be either on a column level or a table level. The column level constraints are applied only to one column, whereas the table level constraints are applied to the whole table.
Following are some of the most commonly used constraints available in SQL. These constraints have already been discussed in SQL - RDBMS Concepts chapter, but it’s worth to revise them at this point.
• NOT NULL Constraint − Ensures that a column cannot have NULL value.
• DEFAULT Constraint − Provides a default value for a column when none is specified.
• UNIQUE Constraint − Ensures that all values in a column are different.
• PRIMARY Key − Uniquely identifies each row/record in a database table.
• FOREIGN Key − Uniquely identifies a row/record in any of the given database table.
• CHECK Constraint − The CHECK constraint ensures that all the values in a column satisfies certain conditions.
• INDEX − Used to create and retrieve data from the database very quickly.
Constraints can be specified when a table is created with the CREATE TABLE statement or you can use the ALTER TABLE statement to create constraints even after the table is created.
1. NOT NULL : By default, a column can hold NULL values. If you do not want a column to have a NULL value, then you need to define such a constraint on this column specifying that NULL is now not allowed for that column.
A NULL is not the same as no data, rather, it represents unknown data.
Example
For example, the following SQL query creates a new table called CUSTOMERS and adds five columns, three of which, are ID NAME and AGE, In this we specify not to accept NULLs −
CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL,
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2),
PRIMARY KEY (ID)
);
If CUSTOMERS table has already been created, then to add a NOT NULL constraint to the SALARY column in Oracle and MySQL, you would write a query like the one that is shown in the following code block.
ALTER TABLE CUSTOMERS
MODIFY SALARY DECIMAL (18, 2) NOT NULL;
2. DEFAULT CONSTRAINT: The DEFAULT constraint provides a default value to a column when the INSERT INTO statement does not provide a specific value.
Example
For example, the following SQL creates a new table called CUSTOMERS and adds five columns. Here, the SALARY column is set to 5000.00 by default, so in case the INSERT INTO statement does not provide a value for this column, then by default this column would be set to 5000.00.
CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL,
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2) DEFAULT 5000.00,
PRIMARY KEY (ID)
);
If the CUSTOMERS table has already been created, then to add a DEFAULT constraint to the SALARY column, you would write a query like the one which is shown in the code block below.
ALTER TABLE CUSTOMERS
MODIFY SALARY DECIMAL (18, 2) DEFAULT 5000.00;
Drop Default Constraint
To drop a DEFAULT constraint, use the following SQL query.
ALTER TABLE CUSTOMERS
ALTER COLUMN SALARY DROP DEFAULT;
3. UNIQUE CONSTRAINT: The UNIQUE Constraint prevents two records from having identical values in a column. In the CUSTOMERS table, for example, you might want to prevent two or more people from having an identical age.
Example
For example, the following SQL query creates a new table called CUSTOMERS and adds five columns. Here, the AGE column is set to UNIQUE, so that you cannot have two records with the same age.
CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL UNIQUE,
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2),
PRIMARY KEY (ID)
);
If the CUSTOMERS table has already been created, then to add a UNIQUE constraint to the AGE column. You would write a statement like the query that is given in the code block below.
ALTER TABLE CUSTOMERS
MODIFY AGE INT NOT NULL UNIQUE;
You can also use the following syntax, which supports naming the constraint in multiple columns as well.
ALTER TABLE CUSTOMERS
ADD CONSTRAINT myUniqueConstraint UNIQUE(AGE, SALARY);
DROP a UNIQUE Constraint
To drop a UNIQUE constraint, use the following SQL query.
ALTER TABLE CUSTOMERS
DROP CONSTRAINT myUniqueConstraint;
If you are using MySQL, then you can use the following syntax −
ALTER TABLE CUSTOMERS
DROP INDEX myUniqueConstraint;
4. PRIMARY KEY: A primary key is a field in a table which uniquely identifies each row/record in a database table. Primary keys must contain unique values. A primary key column cannot have NULL values.
A table can have only one primary key, which may consist of single or multiple fields. When multiple fields are used as a primary key, they are called a composite key.
If a table has a primary key defined on any field(s), then you cannot have two records having the same value of that field(s).
Note − You would use these concepts while creating database tables.
Create Primary Key
Here is the syntax to define the ID attribute as a primary key in a CUSTOMERS table.
CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL,
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2),
PRIMARY KEY (ID)
);
To create a PRIMARY KEY constraint on the "ID" column when the CUSTOMERS table already exists, use the following SQL syntax −
ALTER TABLE CUSTOMER ADD PRIMARY KEY (ID);
NOTE − If you use the ALTER TABLE statement to add a primary key, the primary key column(s) should have already been declared to not contain NULL values (when the table was first created).
For defining a PRIMARY KEY constraint on multiple columns, use the SQL syntax given below.
CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL,
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2),
PRIMARY KEY (ID, NAME)
);
To create a PRIMARY KEY constraint on the "ID" and "NAMES" columns when CUSTOMERS table already exists, use the following SQL syntax.
ALTER TABLE CUSTOMERS
ADD CONSTRAINT PK_CUSTID PRIMARY KEY (ID, NAME);
Delete Primary Key
You can clear the primary key constraints from the table with the syntax given below.
ALTER TABLE CUSTOMERS DROP PRIMARY KEY ;
5.FOREIGN KEY: A foreign key is a key used to link two tables together. This is sometimes also called as a referencing key.
A Foreign Key is a column or a combination of columns whose values match a Primary Key in a different table.
The relationship between 2 tables matches the Primary Key in one of the tables with a Foreign Key in the second table.
If a table has a primary key defined on any field(s), then you cannot have two records having the same value of that field(s).
Example
Consider the structure of the following two tables.
CUSTOMERS table
CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL,
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2),
PRIMARY KEY (ID)
);
ORDERS table
CREATE TABLE ORDERS (
ID INT NOT NULL,
DATE DATETIME,
CUSTOMER_ID INT references CUSTOMERS(ID),
AMOUNT double,
PRIMARY KEY (ID)
);
If the ORDERS table has already been created and the foreign key has not yet been set, the use the syntax for specifying a foreign key by altering a table.
ALTER TABLE ORDERS
ADD FOREIGN KEY (Customer_ID) REFERENCES CUSTOMERS (ID);
DROP a FOREIGN KEY Constraint
To drop a FOREIGN KEY constraint, use the following SQL syntax.
ALTER TABLE ORDERS
DROP FOREIGN KEY;
6.CHECK CONSTRAINT: The CHECK Constraint enables a condition to check the value being entered into a record. If the condition evaluates to false, the record violates the constraint and isn't entered the table.
Example
For example, the following program creates a new table called CUSTOMERS and adds five columns. Here, we add a CHECK with AGE column, so that you cannot have any CUSTOMER who is below 18 years.
CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL CHECK (AGE >= 18),
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2),
PRIMARY KEY (ID)
);
If the CUSTOMERS table has already been created, then to add a CHECK constraint to AGE column, you would write a statement like the one given below.
ALTER TABLE CUSTOMERS
MODIFY AGE INT NOT NULL CHECK (AGE >= 18 );
You can also use the following syntax, which supports naming the constraint in multiple columns as well −
ALTER TABLE CUSTOMERS
ADD CONSTRAINT myCheckConstraint CHECK(AGE >= 18);
DROP a CHECK Constraint
To drop a CHECK constraint, use the following SQL syntax. This syntax does not work with MySQL.
ALTER TABLE CUSTOMERS
DROP CONSTRAINT myCheckConstraint;
Dropping Constraints
Any constraint that you have defined can be dropped using the ALTER TABLE command with the DROP CONSTRAINT option.
For example, to drop the primary key constraint in the EMPLOYEES table, you can use the following command.
ALTER TABLE EMPLOYEES DROP CONSTRAINT EMPLOYEES_PK;
Some implementations may provide shortcuts for dropping certain constraints. For example, to drop the primary key constraint for a table in Oracle, you can use the following command.
ALTER TABLE EMPLOYEES DROP PRIMARY KEY;
Some implementations allow you to disable constraints. Instead of permanently dropping a constraint from the database, you may want to temporarily disable the constraint and then enable it later.
Integrity Constraints
Integrity constraints are used to ensure accuracy and consistency of the data in a relational database. Data integrity is handled in a relational database through the concept of referential integrity.
There are many types of integrity constraints that play a role in Referential Integrity (RI). These constraints include Primary Key, Foreign Key, Unique Constraints and other constraints which are mentioned above.
• NULL Values
The SQL NULL is the term used to represent a missing value. A NULL value in a table is a value in a field that appears to be blank.
A field with a NULL value is a field with no value. It is very important to understand that a NULL value is different than a zero value or a field that contains spaces.
Syntax
The basic syntax of NULL while creating a table.
SQL> CREATE TABLE CUSTOMERS(
ID INT NOT NULL,
NAME VARCHAR (20) NOT NULL,
AGE INT NOT NULL,
ADDRESS CHAR (25) ,
SALARY DECIMAL (18, 2),
PRIMARY KEY (ID)
);
Here, NOT NULL signifies that column should always accept an explicit value of the given data type. There are two columns where we did not use NOT NULL, which means these columns could be NULL.
A field with a NULL value is the one that has been left blank during the record creation.
Example
The NULL value can cause problems when selecting data. However, because when comparing an unknown value to any other value, the result is always unknown and not included in the results. You must use the IS NULL or IS NOT NULL operators to check for a NULL value.
Consider the following CUSTOMERS table having the records as shown below.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | |
| 7 | Muffy | 24 | Indore | |
+----+----------+-----+-----------+----------+
Now, following is the usage of the IS NOT NULLoperator.
SQL> SELECT ID, NAME, AGE, ADDRESS, SALARY
FROM CUSTOMERS
WHERE SALARY IS NOT NULL;
This would produce the following result −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
+----+----------+-----+-----------+----------+
Now, following is the usage of the IS NULL operator.
SQL> SELECT ID, NAME, AGE, ADDRESS, SALARY
FROM CUSTOMERS
WHERE SALARY IS NULL;
This would produce the following result −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 6 | Komal | 22 | MP | |
| 7 | Muffy | 24 | Indore | |
+----+----------+-----+-----------+----------+
• ALTER TABLE Command
The SQL ALTER TABLE command is used to add, delete or modify columns in an existing table. You should also use the ALTER TABLE command to add and drop various constraints on an existing table.
Syntax
The basic syntax of an ALTER TABLE command to add a New Column in an existing table is as follows.
ALTER TABLE table_name ADD column_name datatype;
The basic syntax of an ALTER TABLE command to DROP COLUMN in an existing table is as follows.
ALTER TABLE table_name DROP COLUMN column_name;
The basic syntax of an ALTER TABLE command to change the DATA TYPE of a column in a table is as follows.
ALTER TABLE table_name MODIFY COLUMN column_name datatype;
The basic syntax of an ALTER TABLE command to add a NOT NULL constraint to a column in a table is as follows.
ALTER TABLE table_name MODIFY column_name datatype NOT NULL;
The basic syntax of ALTER TABLE to ADD UNIQUE CONSTRAINT to a table is as follows.
ALTER TABLE table_name
ADD CONSTRAINT MyUniqueConstraint UNIQUE(column1, column2...);
The basic syntax of an ALTER TABLE command to ADD CHECK CONSTRAINT to a table is as follows.
ALTER TABLE table_name
ADD CONSTRAINT MyUniqueConstraint CHECK (CONDITION);
The basic syntax of an ALTER TABLE command to ADD PRIMARY KEY constraint to a table is as follows.
ALTER TABLE table_name
ADD CONSTRAINT MyPrimaryKey PRIMARY KEY (column1, column2...);
The basic syntax of an ALTER TABLE command to DROP CONSTRAINT from a table is as follows.
ALTER TABLE table_name
DROP CONSTRAINT MyUniqueConstraint;
If you're using MySQL, the code is as follows −
ALTER TABLE table_name
DROP INDEX MyUniqueConstraint;
The basic syntax of an ALTER TABLE command to DROP PRIMARY KEY constraint from a table is as follows.
ALTER TABLE table_name
DROP CONSTRAINT MyPrimaryKey;
If you're using MySQL, the code is as follows −
ALTER TABLE table_name
DROP PRIMARY KEY;
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Following is the example to ADD a New Column to an existing table −
ALTER TABLE CUSTOMERS ADD SEX char(1);
Now, the CUSTOMERS table is changed and following would be output from the SELECT statement.
+----+---------+-----+-----------+----------+------+
| ID | NAME | AGE | ADDRESS | SALARY | SEX |
+----+---------+-----+-----------+----------+------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 | NULL |
| 2 | Ramesh | 25 | Delhi | 1500.00 | NULL |
| 3 | kaushik | 23 | Kota | 2000.00 | NULL |
| 4 | kaushik | 25 | Mumbai | 6500.00 | NULL |
| 5 | Hardik | 27 | Bhopal | 8500.00 | NULL |
| 6 | Komal | 22 | MP | 4500.00 | NULL |
| 7 | Muffy | 24 | Indore | 10000.00 | NULL |
+----+---------+-----+-----------+----------+------+
Following is the example to DROP sex column from the existing table.
ALTER TABLE CUSTOMERS DROP SEX;
Now, the CUSTOMERS table is changed and following would be the output from the SELECT statement.
+----+---------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+---------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Ramesh | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | kaushik | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+---------+-----+-----------+----------+
• TRUNCATE TABLE
The SQL TRUNCATE TABLE command is used to delete complete data from an existing table.
You can also use DROP TABLE command to delete complete table but it would remove complete table structure form the database and you would need to re-create this table once again if you wish you store some data.
Syntax
The basic syntax of a TRUNCATE TABLE command is as follows.
TRUNCATE TABLE table_name;
Example
Consider a CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Following is the example of a Truncate command.
SQL > TRUNCATE TABLE CUSTOMERS;
Now, the CUSTOMERS table is truncated and the output from SELECT statement will be as shown in the code block below −
SQL> SELECT * FROM CUSTOMERS;
Empty set (0.00 sec)
• GROUP BY clause
The SQL GROUP BY clause is used in collaboration with the SELECT statement to arrange identical data into groups. This GROUP BY clause follows the WHERE clause in a SELECT statement and precedes the ORDER BY clause.
Syntax
The basic syntax of a GROUP BY clause is shown in the following code block. The GROUP BY clause must follow the conditions in the WHERE clause and must precede the ORDER BY clause if one is used.
SELECT column1, column2
FROM table_name
WHERE [ conditions ]
GROUP BY column1, column2
ORDER BY column1, column2
Example
Consider the CUSTOMERS table is having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
If you want to know the total amount of the salary on each customer, then the GROUP BY query would be as follows.
SQL> SELECT NAME, SUM(SALARY) FROM CUSTOMERS
GROUP BY NAME;
This would produce the following result −
+----------+-------------+
| NAME | SUM(SALARY) |
+----------+-------------+
| Chaitali | 6500.00 |
| Hardik | 8500.00 |
| kaushik | 2000.00 |
| Khilan | 1500.00 |
| Komal | 4500.00 |
| Muffy | 10000.00 |
| Ramesh | 2000.00 |
+----------+-------------+
Now, let us look at a table where the CUSTOMERS table has the following records with duplicate names −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Ramesh | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | kaushik | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Now again, if you want to know the total amount of salary on each customer, then the GROUP BY query would be as follows −
SQL> SELECT NAME, SUM(SALARY) FROM CUSTOMERS
GROUP BY NAME;
This would produce the following result −
+---------+-------------+
| NAME | SUM(SALARY) |
+---------+-------------+
| Hardik | 8500.00 |
| kaushik | 8500.00 |
| Komal | 4500.00 |
| Muffy | 10000.00 |
| Ramesh | 3500.00 |
+---------+-------------+
• Using VIEWS
A view is nothing more than a SQL statement that is stored in the database with an associated name. A view is actually a composition of a table in the form of a predefined SQL query.
A view can contain all rows of a table or select rows from a table. A view can be created from one or many tables which depends on the written SQL query to create a view.
Views, which are a type of virtual tables allow users to do the following −
• Structure data in a way that users or classes of users find natural or intuitive.
• Restrict access to the data in such a way that a user can see and (sometimes) modify exactly what they need and no more.
• Summarize data from various tables which can be used to generate reports.
Creating Views
Database views are created using the CREATE VIEW statement. Views can be created from a single table, multiple tables or another view.
To create a view, a user must have the appropriate system privilege according to the specific implementation.
The basic CREATE VIEW syntax is as follows −
CREATE VIEW view_name AS
SELECT column1, column2.....
FROM table_name
WHERE [condition];
You can include multiple tables in your SELECT statement in a similar way as you use them in a normal SQL SELECT query.
Example
Consider the CUSTOMERS table having the following records −
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 32 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Following is an example to create a view from the CUSTOMERS table. This view would be used to have customer name and age from the CUSTOMERS table.
SQL > CREATE VIEW CUSTOMERS_VIEW AS
SELECT name, age
FROM CUSTOMERS;
Now, you can query CUSTOMERS_VIEW in a similar way as you query an actual table. Following is an example for the same.
SQL > SELECT * FROM CUSTOMERS_VIEW;
This would produce the following result.
+----------+-----+
| name | age |
+----------+-----+
| Ramesh | 32 |
| Khilan | 25 |
| kaushik | 23 |
| Chaitali | 25 |
| Hardik | 27 |
| Komal | 22 |
| Muffy | 24 |
+----------+-----+
The WITH CHECK OPTION
The WITH CHECK OPTION is a CREATE VIEW statement option. The purpose of the WITH CHECK OPTION is to ensure that all UPDATE and INSERTs satisfy the condition(s) in the view definition.
If they do not satisfy the condition(s), the UPDATE or INSERT returns an error.
The following code block has an example of creating same view CUSTOMERS_VIEW with the WITH CHECK OPTION.
CREATE VIEW CUSTOMERS_VIEW AS
SELECT name, age
FROM CUSTOMERS
WHERE age IS NOT NULL
WITH CHECK OPTION;
The WITH CHECK OPTION in this case should deny the entry of any NULL values in the view's AGE column, because the view is defined by data that does not have a NULL value in the AGE column.
Updating a View
A view can be updated under certain conditions which are given below −
• The SELECT clause may not contain the keyword DISTINCT.
• The SELECT clause may not contain summary functions.
• The SELECT clause may not contain set functions.
• The SELECT clause may not contain set operators.
• The SELECT clause may not contain an ORDER BY clause.
• The FROM clause may not contain multiple tables.
• The WHERE clause may not contain subqueries.
• The query may not contain GROUP BY or HAVING.
• Calculated columns may not be updated.
• All NOT NULL columns from the base table must be included in the view in order for the INSERT query to function.
So, if a view satisfies all the above-mentioned rules then you can update that view. The following code block has an example to update the age of Ramesh.
SQL > UPDATE CUSTOMERS_VIEW
SET AGE = 35
WHERE name = 'Ramesh';
This would ultimately update the base table CUSTOMERS and the same would reflect in the view itself. Now, try to query the base table and the SELECT statement would produce the following result.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 35 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 6 | Komal | 22 | MP | 4500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Inserting Rows into a View
Rows of data can be inserted into a view. The same rules that apply to the UPDATE command also apply to the INSERT command.
Here, we cannot insert rows in the CUSTOMERS_VIEW because we have not included all the NOT NULL columns in this view, otherwise you can insert rows in a view in a similar way as you insert them in a table.
Deleting Rows into a View
Rows of data can be deleted from a view. The same rules that apply to the UPDATE and INSERT commands apply to the DELETE command.
Following is an example to delete a record having AGE = 22.
SQL > DELETE FROM CUSTOMERS_VIEW
WHERE age = 22;
This would ultimately delete a row from the base table CUSTOMERS and the same would reflect in the view itself. Now, try to query the base table and the SELECT statement would produce the following result.
+----+----------+-----+-----------+----------+
| ID | NAME | AGE | ADDRESS | SALARY |
+----+----------+-----+-----------+----------+
| 1 | Ramesh | 35 | Ahmedabad | 2000.00 |
| 2 | Khilan | 25 | Delhi | 1500.00 |
| 3 | kaushik | 23 | Kota | 2000.00 |
| 4 | Chaitali | 25 | Mumbai | 6500.00 |
| 5 | Hardik | 27 | Bhopal | 8500.00 |
| 7 | Muffy | 24 | Indore | 10000.00 |
+----+----------+-----+-----------+----------+
Dropping Views
Obviously, where you have a view, you need a way to drop the view if it is no longer needed. The syntax is very simple and is given below −
DROP VIEW view_name;
Following is an example to drop the CUSTOMERS_VIEW from the CUSTOMERS table.
DROP VIEW CUSTOMERS_VIEW;
Queries Using aggregate functions :-
1. 2nd highest Salary :
Syntax:
SELECT MAX(SALARY)
FROM TABLENAME
WHERE SALARY NOT IN ( SELECT MAX(SALARY) FROM TABLENAME);
2. 2ND minimum Salary
Syntax:
SELECT MIN(SALARY)
FROM TABLENAME
WHERE SALARY NOT IN ( SELECT MIN(SALARY) FROM TABLENAME);
3. Nth Highest Salary:
Syntax:
SELECT MIN(SALARY)
FROM TABLENAME
WHERE SALARY IN (SELECT TOP Nth SALARY FROM TABLENAME
ORDER BY SALARY DESC);
4. Nth Minimum Salary :
Syntax:
SELECT MAX (SALARY)
FROM TABLENAME
WHERE SALARY IN (SELECT TOP Nth SALARY FROM TABLENAME
ORDER BY SALARY);
IN Operator The IN operator allows you to specify multiple values in a WHERE clause. The IN operator is a shorthand for multiple OR conditions. IN Syntax SELECT column_name(s) FROM table_name WHERE column_name IN (value1, value2, ...);
Or
SELECT column_name(s) FROM table_name WHERE column_name IN (SELECT STATEMENT);
For ex: The following SQL statement selects all customers that are located in "Germany", "France" or "UK":
SELECT * FROM Customers WHERE Country IN ('Germany', 'France', 'UK');
Ex 2: The following SQL statement selects all customers that are NOT located in "Germany", "France" or "UK":
SELECT * FROM Customers WHERE Country NOT IN ('Germany', 'France', 'UK');
The SQL BETWEEN Operator The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates. The BETWEEN operator is inclusive: begin and end values are included. BETWEEN Syntax SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value1 AND value2;
Ex: The following SQL statement selects all products with a price between 10 and 20:
SELECT * FROM Products WHERE Price BETWEEN 10 AND 20; BETWEEN Text Values Example The following SQL statement selects all products with a ProductName between Carnarvon Tigers and Mozzarella di Giovanni: Ex: SELECT * FROM Products WHERE ProductName BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni' ORDER BY ProductName;
Union and Union ALL UNION The UNION command is used to select related information from two tables, which is like a JOIN command. However, when using UNION command, all the selected columns need to be of the same data type. With UNION, only distinct values are selected. UNION ALL UNION ALL command is equal to UNION command, except that UNION ALL selects all the values. The difference between Union and Union all is that Union all will not eliminate duplicate rows, instead it just pulls all the rows from all the tables fitting your query specifics and combines them into a table. A UNION statement effectively does a SELECT DISTINCT on the results set. If you know that all the records returned are unique from your union, use UNION ALL instead, it gives faster results. Example Table 1 : First,Second,Third,Fourth,Fifth Table 2 : First,Second,Fifth,Sixth Result Set UNION: First,Second,Third,Fourth,Fifth,Sixth (This will remove duplicate values) UNION ALL: First,First,Second,Second,Third,Fourth,Fifth,Fifth,Sixth,Sixth (This will repeat values)
The SQL COUNT(), AVG() and SUM() Functions The COUNT() function returns the number of rows that matches a specified criterion. COUNT() Syntax SELECT COUNT(column_name) FROM table_name WHERE condition;
COUNT() Example The following SQL statement finds the number of products: SELECT COUNT(ProductID) FROM Products;
The AVG() function returns the average value of a numeric column. AVG() Syntax SELECT AVG(column_name) FROM table_name WHERE condition; AVG() Example The following SQL statement finds the average price of all products: SELECT AVG(Price) FROM Products; The SUM() function returns the total sum of a numeric column. SUM() Syntax SELECT SUM(column_name) FROM table_name WHERE condition;
SUM() Example
The following SQL statement finds the sum of the "Quantity" fields in the "OrderDetails" table: SELECT SUM(Quantity) FROM OrderDetails;
The SQL MIN() and MAX() Functions The MIN() function returns the smallest value of the selected column. The MAX() function returns the largest value of the selected column. MIN() Syntax SELECT MIN(column_name) FROM table_name WHERE condition;
Min Example The following SQL statement finds the price of the cheapest product:
SELECT MIN(Price) AS SmallestPrice FROM Products; MAX() Syntax SELECT MAX(column_name) FROM table_name WHERE condition;
MAX() Example The following SQL statement finds the price of the most expensive product: SELECT MAX(Price) AS LargestPrice FROM Products;
The FIRST() Function The FIRST() function returns the first value of the selected column. SQL FIRST() Syntax SELECT FIRST(column_name) FROM table_name;
SQL FIRST() Example The following SQL statement selects the first value of the "CustomerName" column from the "Customers" table: SELECT FIRST(CustomerName) AS FirstCustomer FROM Customers; LAST
The LAST() Function The LAST() function returns the last value of the selected column. SQL LAST() Syntax SELECT LAST(column_name) FROM table_name; SQL LAST() Example The following SQL statement selects the last value of the "CustomerName" column from the "Customers" table: SELECT LAST(CustomerName) AS LastCustomer FROM Customers;
The HAVING Clause The HAVING clause was added to SQL because the WHERE keyword could not be used with aggregate functions.
Having:- used to select records which satisfy the given condition and also it is used with aggregate function. SQL HAVING Syntax SELECT column_name(s) FROM table_name WHERE condition GROUP BY column_name(s) HAVING condition ORDER BY column_name(s);
SQL HAVING Examples The following SQL statement lists the number of customers in each country. Only include countries with more than 5 customers: SELECT COUNT(CustomerID), Country FROM Customers GROUP BY Country HAVING COUNT(CustomerID) > 5;
SQL Views SQL CREATE VIEW Statement In SQL, a view is a virtual table based on the result-set of an SQL statement. A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database. You can add SQL statements and functions to a view and present the data as if the data were coming from one single table. A view is created with the CREATE VIEW statement.
VIEW: CREATES A VIRTUAL TABLE BASED ON RESULT SET OF SQL STATEMENT. CREATE VIEW Syntax CREATE VIEW view_name AS SELECT column1, column2, ... FROM table_name WHERE condition; SQL CREATE VIEW Examples The following SQL creates a view that shows all customers from Brazil: CREATE VIEW [Brazil Customers] AS SELECT CustomerName, ContactName FROM Customers WHERE Country = 'Brazil'; We can query the view above as follows: SELECT * FROM [Brazil Customers]; TABLE 1 TID, TNAME, TCITY, TID - PK TABLE 2 TDATE, T2ID2, T2NAME, TID TID-FK, T2ID2 - PK


