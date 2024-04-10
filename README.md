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
