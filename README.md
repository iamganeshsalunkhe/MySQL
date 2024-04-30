# MySQL
MySQLDB is a comprehensive repository for MySQL database management, featuring a collection of scripts, utilities, and resources tailored to streamline MySQL database development, administration, and optimization.


### What is MySQL?
MySQL is a relational database management system.

MySQL is open-source.

MySQL is free.

MySQL is ideal for both small and large applications.

MySQL is very fast, reliable, scalable, and easy to use.

MySQL is cross-platform.

MySQL is compliant with the ANSI SQL standard.

MySQL was first released in 1995.

MySQL is developed, distributed, and supported by Oracle Corporation.

MySQL is named after co-founder Monty Widenius's daughter: My


### Who Uses MySQL?
Huge websites like Facebook, Twitter, Airbnb, Booking.com, Uber, GitHub, YouTube, etc.

Content Management Systems like WordPress, Drupal, Joomla!, Contao, etc.

A very large number of web developers around the world


### Show Data On Your Web Site
To build a web site that shows data from a database, you will need:

An RDBMS database program (like MySQL).

A server-side scripting language, like PHP.

To use SQL to get the data you want.


To use HTML / CSS to style the page.

### What is RDBMS?
RDBMS stands for Relational Database Management System.

RDBMS is a program used to maintain a relational database.

RDBMS is the basis for all modern database systems such as MySQL, Microsoft SQL Server, Oracle, and Microsoft Access.

RDBMS uses SQL queries to access the data in the database.

### What is a Database Table?
A table is a collection of related data entries, and it consists of columns and rows.

A column holds specific information about every record in the table.

A record (or row) is each individual entry that exists in a table.

Look at a selection from the Northwind "Customers" table:


<img width="586" alt="Screenshot 2024-04-03 161044" src="https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/99ade343-501e-49f8-bc4f-09faf587a8c9">


### What is a Relational Database?
A relational database defines database relationships in the form of tables. The tables are related to each other - based on data common to each.


Look at the following three tables "Customers", "Orders", and "Shippers" from the Northwind database:


<img width="580" alt="Screenshot 2024-04-03 161241" src="https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/2e71f98a-76de-40ce-a0f3-74f35bc62274">

#### The relationship between the "Customers" table and the "Orders" table is the CustomerID column.


### What is SQL?

SQL is the standard language for dealing with Relational Databases.


SQL is used to insert, search, update, and delete database records.

#### SQL keywords are NOT case sensitive: select is the same as SELECT.


Semicolon after SQL Statements?

Some database systems require a semicolon at the end of each SQL statement.

Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.



Some of The Most Important SQL Commands

**SELECT** - extracts data from a database

**UPDATE** - updates data in a database

**DELETE** - deletes data from a database

**INSERT INTO** - inserts new data into a database

**CREATE DATABASE** - creates a new database

**ALTER DATABASE** - modifies a database

**CREATE TABLE** - creates a new table

**ALTER TABLE** - modifies a table

**DROP TABLE** - deletes a table

**CREATE INDEX** - creates an index (search key)

**DROP INDEX** - deletes an index


### The MySQL SELECT Statement.

The SELECT statement is used to select data from a database.

The data returned is stored in a result table, called the result-set.

```
SELECT * FROM table_name;
```

### SELECT * Example

The following SQL statement selects ALL the columns from the "Customers" table:

`SELECT * FROM Customers;`


###  The MySQL WHERE Clause

The WHERE clause is used to filter records.

It is used to extract only those records that fulfill a specified condition.

```
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```


#### Operators in The WHERE Clause

The following operators can be used in the WHERE clause:


<img width="511" alt="Screenshot 2024-04-10 162309" src="https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/6769935b-47af-4356-b018-c23f9f48693f">


### The MySQL AND, OR and NOT Operators

The WHERE clause can be combined with AND, OR, and NOT operators.

The AND and OR operators are used to filter records based on more than one condition:

The AND operator displays a record if all the conditions separated by AND are TRUE.

The OR operator displays a record if any of the conditions separated by OR is TRUE.

The NOT operator displays a record if the condition(s) is NOT TRUE.


#### AND Syntax:
```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```


#### OR Syntax
```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
```

#### NOT Syntax
```
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```

#### Combining AND, OR and NOT

You can also combine the AND, OR and NOT operators.


### The MySQL ORDER BY Keyword

The ORDER BY keyword is used to sort the result-set in ascending or descending order.


The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.


#### ORDER BY Syntax
```
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

### The MySQL INSERT INTO Statement

The INSERT INTO statement is used to insert new records in a table.

#### INSERT INTO Syntax

It is possible to write the INSERT INTO statement in two ways:

1. Specify both the column names and the values to be inserted:
```
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the INSERT INTO syntax would be as follows

```
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

### What is a NULL Value?

A field with a NULL value is a field with no value.

If a field in a table is optional, it is possible to insert a new record or update a record without adding a value to this field. Then, the field will be saved with a NULL value.

#### A NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!

#### How to Test for NULL Values?

It is not possible to test for NULL values with comparison operators, such as =, <, or <>.

We will have to use the IS NULL and IS NOT NULL operators instea

#### IS NULL SYNTAX
```
SELECT column_names
FROM table_name
WHERE column_name IS NULL;
```

#### IS NOT NULL SYNTAX

```
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
```

### The MySQL UPDATE Statement

The UPDATE statement is used to modify the existing records in a table.

#### UPDATE Syntax

```
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

### The MySQL DELETE Statement
The DELETE statement is used to delete existing records in a table.

#### DELETE Syntax

`DELETE FROM table_name WHERE condition;`

#### Delete All Records

It is possible to delete all rows in a table without deleting the table. This means that the table structure, attributes, and indexes will be intact:

`DELETE FROM table_name;`

### The MySQL LIMIT Clause

The LIMIT clause is used to specify the number of records to return.

The LIMIT clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.

#### LIMIT Syntax

```
SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number;
```
#### MySQL LIMIT Examples

The following SQL statement selects the first three records from the "Customers" table:

```
SELECT * FROM Customers
LIMIT 3;
```

##### What if we want to select records 4 - 6 (inclusive)?

MySQL provides a way to handle this: by using OFFSET.

The SQL query below says "return only 3 records, start on record 4 (OFFSET 3)":

```
SELECT * FROM Customers
LIMIT 3 OFFSET 3;
```


### MySQL MIN() and MAX() Functions

The MIN() function returns the smallest value of the selected column.

The MAX() function returns the largest value of the selected column.

#### MIN() Syntax
```
SELECT MIN(column_name)
FROM table_name
WHERE condition;
```

#### MAX() Syntax
```
SELECT MAX(column_name)
FROM table_name
WHERE condition;
```

### MySQL COUNT(), AVG() and SUM() Functions

The COUNT() function returns the number of rows that matches a specified criterion.

#### COUNT() Syntax
```
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```

#### AVG() Syntax 

The AVG() function returns the average value of a numeric column. 

```
SELECT AVG(column_name)
FROM table_name
WHERE condition;
```

#### SUM() Syntax

The SUM() function returns the total sum of a numeric column. 

```
SELECT SUM(column_name)
FROM table_name
WHERE condition;
```


### The MySQL LIKE Operator

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

There are two wildcards often used in conjunction with the LIKE operator:

The percent sign (%) represents zero, one, or multiple characters
The underscore sign (_) represents one, single character
The percent sign and the underscore can also be used in combinations!

#### LIKE Syntax

```
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```

### MySQL Wildcard Characters

A wildcard character is used to substitute one or more characters in a string.

Wildcard characters are used with the LIKE operator. The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

![Screenshot 2024-04-22 125919](https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/9dcf0c36-4420-4d83-8d18-9ebc9b754308)

The wildcards can also be used in combinations!

Here are some examples showing different LIKE operators with '%' and '_' wildcards:



![Screenshot 2024-04-22 125950](https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/4cf1adfa-284f-48b7-b2cd-c751269a993f)


### The MySQL IN Operator
The IN operator allows you to specify multiple values in a WHERE clause.

The IN operator is a shorthand for multiple OR conditions.

#### IN Syntax

```
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);
```
## OR 

```
SELECT column_name(s)
FROM table_name
WHERE column_name IN (SELECT STATEMENT);
```


### The MySQL BETWEEN Operator

The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.

The BETWEEN operator is inclusive: begin and end values are included.

#### BETWEEN Syntax

```
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

#### NOT BETWEEN Example

To display the products outside the range of the previous example, use NOT BETWEEN:


```
SELECT * FROM Products
WHERE Price NOT BETWEEN 10 AND 20;
```

#### BETWEEN with IN Example

The following SQL statement selects all products with a price between 10 and 20. In addition; do not show products with a CategoryID of 1,2, or 3:


```
SELECT * FROM Products
WHERE Price BETWEEN 10 AND 20
AND CategoryID NOT IN (1,2,3);
```

### MySQL Aliases

Aliases are used to give a table, or a column in a table, a temporary name.

Aliases are often used to make column names more readable.

An alias only exists for the duration of that query.

An alias is created with the AS keyword.

#### Alias Column Syntax

```
SELECT column_name AS alias_name
FROM table_name;
```
#### Alias Table Syntax

```
SELECT column_name(s)
FROM table_name AS alias_name;
```

### MySQL Joining Tables

A JOIN clause is used to combine rows from two or more tables, based on a related column between them.

Let's look at a selection from the "Orders" table:

![Screenshot 2024-04-22 130656](https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/d0308ee8-87b1-4278-a73d-58eaf2aec7a9)

Then, look at a selection from the "Customers" table:

![Screenshot 2024-04-22 130711](https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/cb22c30e-a637-47f7-acdf-5ba69fa5a10b)


##### Notice that the "CustomerID" column in the "Orders" table refers to the "CustomerID" in the "Customers" table. The relationship between the two tables above is the "CustomerID" column.

Then, we can create the following SQL statement (that contains an INNER JOIN), that selects records that have matching values in both tables:

```
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```

and it will produce something like this:

![Screenshot 2024-04-22 130734](https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/bcf44387-a897-458f-8c73-698443bb9f7a)


##### Supported Types of Joins in MySQL

INNER JOIN: Returns records that have matching values in both tables

LEFT JOIN: Returns all records from the left table, and the matched records from the right table

RIGHT JOIN: Returns all records from the right table, and the matched records from the left table

CROSS JOIN: Returns all records from both tables


### MySQL INNER JOIN Keyword

The INNER JOIN keyword selects records that have matching values in both tables.


#### INNER JOIN Syntax
```
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

### MySQL LEFT JOIN Keyword

The LEFT JOIN keyword returns all records from the left table (table1), and the matching records (if any) from the right table (table2).
#### LEFT JOIN Syntax

```
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

### MySQL RIGHT JOIN Keyword

The RIGHT JOIN keyword returns all records from the right table (table2), and the matching records (if any) from the left table (table1).

#### RIGHT JOIN Syntax
```
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```

### SQL CROSS JOIN Keyword

The CROSS JOIN keyword returns all records from both tables (table1 and table2).

#### CROSS JOIN Syntax
```
SELECT column_name(s)
FROM table1
CROSS JOIN table2;
```

### MySQL Self Join

A self join is a regular join, but the table is joined with itself.

#### Self Join Syntax
```
SELECT column_name(s)
FROM table1 T1, table1 T2
WHERE condition;
```

### The MySQL UNION Operator

The UNION operator is used to combine the result-set of two or more SELECT statements.

Every SELECT statement within UNION must have the same number of columns.

The columns must also have similar data types.

The columns in every SELECT statement must also be in the same order.

#### UNION Syntax
```
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

#### UNION ALL Syntax

The UNION operator selects only distinct values by default. To allow duplicate values, use UNION ALL:
```
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```

### The MySQL GROUP BY Statement

The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of customers in each country".

The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) to group the result-set by one or more columns.

#### GROUP BY Syntax

```
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```

### The MySQL HAVING Clause

The HAVING clause was added to SQL because the WHERE keyword cannot be used with aggregate functions.

#### HAVING Syntax

```
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

### The MySQL EXISTS Operator

The EXISTS operator is used to test for the existence of any record in a subquery.

The EXISTS operator returns TRUE if the subquery returns one or more records.

#### EXISTS Syntax
```
SELECT column_name(s)
FROM table_name
WHERE EXISTS
(SELECT column_name FROM table_name WHERE condition);
```

### The MySQL ANY and ALL Operators

The ANY and ALL operators allow you to perform a comparison between a single column value and a range of other values.


#### The ANY operator:

returns a boolean value as a result.

returns TRUE if ANY of the subquery values meet the condition.

ANY means that the condition will be true if the operation is true for any of the values in the range.

#### ANY Syntax

```
SELECT column_name(s)
FROM table_name
WHERE column_name operator ANY
  (SELECT column_name
  FROM table_name
  WHERE condition);
```

#### The ALL operator:

returns a boolean value as a result.

returns TRUE if ALL of the subquery values meet the condition.

is used with SELECT, WHERE and HAVING statements.

#### ALL means that the condition will be true only if the operation is true for all values in the range.
```
ALL Syntax With SELECT
SELECT ALL column_name(s)
FROM table_name
WHERE condition;
```
#### ALL Syntax With WHERE or HAVING

```
SELECT column_name(s)
FROM table_name
WHERE column_name operator ALL
  (SELECT column_name
  FROM table_name
  WHERE condition);
```

### The MySQL INSERT INTO SELECT Statement

The INSERT INTO SELECT statement copies data from one table and inserts it into another table.

The INSERT INTO SELECT statement requires that the data types in source and target tables matches.

Note: The existing records in the target table are unaffected.

#### INSERT INTO SELECT Syntax
Copy all columns from one table to another table:
```
INSERT INTO table2
SELECT * FROM table1
WHERE condition;
```
Copy only some columns from one table into another table:

```
INSERT INTO table2 (column1, column2, column3, ...)
SELECT column1, column2, column3, ...
FROM table1
WHERE condition;
```


### The MySQL CASE Statement

The CASE statement goes through conditions and returns a value when the first condition is met (like an if-then-else statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause.

If there is no ELSE part and no conditions are true, it returns NULL.

#### CASE Syntax

```
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

### MySQL Comments

Comments are used to explain sections of SQL statements, or to prevent execution of SQL statements.

#### Single Line Comments

Single line comments start with --.

Any text between -- and the end of the line will be ignored (will not be executed).

The following example uses a single-line comment as an explanation:

```
-- Select all:
SELECT * FROM Customers;
```
The following example uses a single-line comment to ignore the end of a line:

`SELECT * FROM Customers -- WHERE City='Berlin';`

The following example uses a single-line comment to ignore a statement:

```
-- SELECT * FROM Customers;
SELECT * FROM Products;`
```


### Multi-line Comments

Multi-line comments start with /* and end with */.

Any text between /* and */ will be ignored.

The following example uses a multi-line comment as an explanation:

```
/*Select all the columns
of all the records
in the Customers table:*/
SELECT * FROM Customers;
```

To ignore just a part of a statement, also use the /* */ comment.

The following example uses a comment to ignore part of a line:

`SELECT CustomerName, /*City,*/ Country FROM Customers;`

The following example uses a comment to ignore part of a statement:


```
SELECT * FROM Customers WHERE (CustomerName LIKE 'L%'
OR CustomerName LIKE 'R%' /*OR CustomerName LIKE 'S%'
OR CustomerName LIKE 'T%'*/ OR CustomerName LIKE 'W%')
AND Country='USA'
ORDER BY CustomerName;
```


### MySQL Operators:

#### MySQL Logical Oprators

<img width="522" alt="Screenshot 2024-04-25 151723" src="https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/92e6e153-34bf-473e-897a-e1cd09fb39d1">

#### MySQL Compound Operators


<img width="532" alt="Screenshot 2024-04-25 151846" src="https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/7d9888fd-f120-4935-941b-f29ae55c59b4">

#### MySQL Comparison Operators

<img width="497" alt="Screenshot 2024-04-25 152000" src="https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/ff871a82-2696-41a8-be62-310564c37cb5">

#### MySQL Bitwise Operators


<img width="569" alt="Screenshot 2024-04-25 152048" src="https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/ede72df9-115b-4d3e-bedf-eeb56f479c3a">

#### MySQL Arithmetic Operators

<img width="519" alt="Screenshot 2024-04-25 152128" src="https://github.com/iamganeshsalunkhe/MySQL/assets/143490640/56dcc7e3-437e-4b2f-a698-559ef309aa32">




### The MySQL CREATE DATABASE Statement

The CREATE DATABASE statement is used to create a new SQL database.

Syntax:
`CREATE DATABASE databasename;`

### The MySQL DROP DATABASE Statement

The DROP DATABASE statement is used to drop an existing SQL database.

Syntax


`DROP DATABASE databasename;`


### The MySQL CREATE TABLE Statement
The CREATE TABLE statement is used to create a new table in a database.

Syntax
```
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
```

The column parameters specify the names of the columns of the table.

The datatype parameter specifies the type of data the column can hold (e.g. varchar, integer, date, etc.).


### The MySQL DROP TABLE Statement

The DROP TABLE statement is used to drop an existing table in a database.

Syntax

`DROP TABLE table_name;`

### MySQL TRUNCATE TABLE
The TRUNCATE TABLE statement is used to delete the data inside a table, but not the table itself.

Syntax

`TRUNCATE TABLE table_name;`

### MySQL ALTER TABLE Statement

The ALTER TABLE statement is used to add, delete, or modify columns in an existing table.

The ALTER TABLE statement is also used to add and drop various constraints on an existing table

#### ALTER TABLE - ADD Column
To add a column in a table, use the following syntax:
```
ALTER TABLE table_name
ADD column_name datatype;
```

#### ALTER TABLE - DROP COLUMN
To delete a column in a table, use the following syntax (notice that some database systems don't allow deleting a column):
```
ALTER TABLE table_name
DROP COLUMN column_name;
```

#### ALTER TABLE - MODIFY COLUMN
To change the data type of a column in a table, use the following syntax:
```
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;
```

### Create Constraints

Constraints can be specified when the table is created with the CREATE TABLE statement, or after the table is created with the ALTER TABLE statement.

Syntax
```
CREATE TABLE table_name (
    column1 datatype constraint,
    column2 datatype constraint,
    column3 datatype constraint,
    ....
);
```

### MySQL Constraints

SQL constraints are used to specify rules for the data in a table.

Constraints are used to limit the type of data that can go into a table. This ensures the accuracy and reliability of the data in the table. If there is any violation between the constraint and the data action, the action is aborted.

Constraints can be column level or table level. Column level constraints apply to a column, and table level constraints apply to the whole table.

The following constraints are commonly used in SQL:

#### NOT NULL - Ensures that a column cannot have a NULL value

#### UNIQUE - Ensures that all values in a column are different

#### PRIMARY KEY - A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table

#### FOREIGN KEY - Prevents actions that would destroy links between tables

#### CHECK - Ensures that the values in a column satisfies a specific condition

#### DEFAULT - Sets a default value for a column if no value is specified

#### CREATE INDEX - Used to create and retrieve data from the database very quickly

### MySQL NOT NULL Constraint

By default, a column can hold NULL values.


The NOT NULL constraint enforces a column to NOT accept NULL values.

This enforces a field to always contain a value, which means that you cannot insert a new record, or update a record without adding a value to this field.

##### NOT NULL on CREATE TABLE

The following SQL ensures that the "ID", "LastName", and "FirstName" columns will NOT accept NULL values when the "Persons" table is created:

```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255) NOT NULL,
    Age int
);
```
##### NOT NULL on ALTER TABLE
To create a NOT NULL constraint on the "Age" column when the "Persons" table is already created, use the following SQL:

Example
```
ALTER TABLE Persons
MODIFY Age int NOT NULL;

```

### MySQL UNIQUE Constraint

The UNIQUE constraint ensures that all values in a column are different.

Both the UNIQUE and PRIMARY KEY constraints provide a guarantee for uniqueness for a column or set of columns.

A PRIMARY KEY constraint automatically has a UNIQUE constraint.

However, you can have many UNIQUE constraints per table, but only one PRIMARY KEY constraint per table.

UNIQUE Constraint on CREATE TABLE

The following SQL creates a UNIQUE constraint on the "ID" column when the "Persons" table is created:
```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    UNIQUE (ID)
);
```
To name a UNIQUE constraint, and to define a UNIQUE constraint on multiple columns, use the following SQL syntax:
```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT UC_Person UNIQUE (ID,LastName)
);
```

#### UNIQUE Constraint on ALTER TABLE

To create a UNIQUE constraint on the "ID" column when the table is already created, use the following SQL:
```
ALTER TABLE Persons
ADD UNIQUE (ID);
```

To name a UNIQUE constraint, and to define a UNIQUE constraint on multiple columns, use the following SQL syntax:
```

ALTER TABLE Persons
ADD CONSTRAINT UC_Person UNIQUE (ID,LastName);
```
#### DROP a UNIQUE Constraint

To drop a UNIQUE constraint, use the following SQL:
```
ALTER TABLE Persons
DROP INDEX UC_Person;

```

### MySQL PRIMARY KEY Constraint
The PRIMARY KEY constraint uniquely identifies each record in a table.

Primary keys must contain UNIQUE values, and cannot contain NULL values.

A table can have only ONE primary key; and in the table, this primary key can consist of single or multiple columns (fields).

PRIMARY KEY on CREATE TABLE

The following SQL creates a PRIMARY KEY on the "ID" column when the "Persons" table is created:

```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);
```

To allow naming of a PRIMARY KEY constraint, and for defining a PRIMARY KEY constraint on multiple columns, use the following SQL syntax:

```

CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT PK_Person PRIMARY KEY (ID,LastName)
);
```


#### PRIMARY KEY on ALTER TABLE
To create a PRIMARY KEY constraint on the "ID" column when the table is already created, use the following SQL:
```
ALTER TABLE Persons
ADD PRIMARY KEY (ID);
```

#### DROP a PRIMARY KEY Constraint
To drop a PRIMARY KEY constraint, use the following SQL:
```
ALTER TABLE Persons
DROP PRIMARY KEY;
```

### MySQL FOREIGN KEY Constraint

The FOREIGN KEY constraint is used to prevent actions that would destroy links between tables.


A FOREIGN KEY is a field (or collection of fields) in one table, that refers to the PRIMARY KEY in another table.

The table with the foreign key is called the child table, and the table with the primary key is called the referenced or parent table


### MySQL CHECK Constraint

The CHECK constraint is used to limit the value range that can be placed in a column.

If you define a CHECK constraint on a column it will allow only certain values for this column.

If you define a CHECK constraint on a table it can limit the values in certain columns based on values in other columns in the row.

#### CHECK on CREATE TABLE

The following SQL creates a CHECK constraint on the "Age" column when the "Persons" table is created. The CHECK constraint ensures that the age of a person must be 18, or older:

```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
);
```

To allow naming of a CHECK constraint, and for defining a CHECK constraint on multiple columns, use the following SQL syntax:

```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255),
    CONSTRAINT CHK_Person CHECK (Age>=18 AND City='Sandnes')
);
```

#### CHECK on ALTER TABLE

To create a CHECK constraint on the "Age" column when the table is already created, use the following SQL:

```
ALTER TABLE Persons
ADD CHECK (Age>=18);
```

To allow naming of a CHECK constraint, and for defining a CHECK constraint on multiple columns, use the following SQL syntax:
```
ALTER TABLE Persons
ADD CONSTRAINT CHK_PersonAge CHECK (Age>=18 AND City='Sandnes');
```

#### DROP a CHECK Constraint
To drop a CHECK constraint, use the following SQL:
```
ALTER TABLE Persons
DROP CHECK CHK_PersonAge;
```
### MySQL DEFAULT Constraint
The DEFAULT constraint is used to set a default value for a column.

The default value will be added to all new records, if no other value is specified.

#### DEFAULT on CREATE TABLE

The following SQL sets a DEFAULT value for the "City" column when the "Persons" table is created:

```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255) DEFAULT 'Sandnes'
);
```

The DEFAULT constraint can also be used to insert system values, by using functions like CURRENT_DATE():

```
CREATE TABLE Orders (
    ID int NOT NULL,
    OrderNumber int NOT NULL,
    OrderDate date DEFAULT CURRENT_DATE()
);
```


#### DEFAULT on ALTER TABLE

To create a DEFAULT constraint on the "City" column when the table is already created, use the following SQL:

```
ALTER TABLE Persons
ALTER City SET DEFAULT 'Sandnes';
```

#### DROP a DEFAULT Constraint

To drop a DEFAULT constraint, use the following SQL:

```
ALTER TABLE Persons
ALTER City DROP DEFAULT;
```

### What is an AUTO INCREMENT Field?
Auto-increment allows a unique number to be generated automatically when a new record is inserted into a table.

Often this is the primary key field that we would like to be created automatically every time a new record is inserted.

##### MySQL AUTO_INCREMENT Keyword

MySQL uses the AUTO_INCREMENT keyword to perform an auto-increment feature.

By default, the starting value for AUTO_INCREMENT is 1, and it will increment by 1 for each new record.

The following SQL statement defines the "Personid" column to be an auto-increment primary key field in the "Persons" table:



```
CREATE TABLE Persons (
    Personid int NOT NULL AUTO_INCREMENT,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (Personid)
);
```

To let the AUTO_INCREMENT sequence start with another value, use the following SQL statement:

`ALTER TABLE Persons AUTO_INCREMENT=100;`

### MySQL Dates

##### The most difficult part when working with dates is to be sure that the format of the date you are trying to insert, matches the format of the date column in the database.

As long as your data contains only the date portion, your queries will work as expected. However, if a time portion is involved, it gets more complicated.

MySQL Date Data Types

MySQL comes with the following data types for storing a date or a date/time value in the database:

DATE - format YYYY-MM-DD.

DATETIME - format: YYYY-MM-DD HH:MI:SS.

TIMESTAMP - format: YYYY-MM-DD HH:MI:SS.

YEAR - format YYYY or YY.

