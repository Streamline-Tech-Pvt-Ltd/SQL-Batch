DAY 1 – SQL INSTALLATION

1. SQL SOFTWARE / TOOLS

For learning SQL, we can use different tools:

1. MySQL Workbench
2. MySQL Command Line Client
3. PostgreSQL pgAdmin

2. MYSQL INSTALLATION

MySQL is a database management system used to store,
manage and retrieve data.

During MySQL installation, we can use:

1. MySQL Server
2. MySQL Workbench
3. MySQL Command Line Client


# MySQL Server:
It stores and manages databases and data.

# MySQL Workbench:
It is a GUI (Graphical User Interface) tool used to work
with MySQL databases.

# MySQL Command Line Client:
It is a command-line tool used to connect to MySQL Server
and execute SQL commands.


# MYSQL WORKBENCH

MySQL Workbench is a GUI tool used to work with MySQL.

Using MySQL Workbench, we can:

1. Create Database
2. Create Table
3. Insert Data
4. Read Data
5. Update Data
6. Delete Data
7. Run SQL Queries


Example:

CREATE DATABASE college;

USE college;

CREATE TABLE student (
    student_id INT,
    student_name VARCHAR(50),
    age INT
);

To see table data:

SELECT * FROM student;


# MYSQL COMMAND LINE CLIENT


MySQL Command Line Client allows us to work with MySQL
using commands in the command prompt.

Example:

mysql -u root -p

After this command, we enter the MySQL password.


# POSTGRESQL AND pgAdmin

PostgreSQL is a relational database management system.

pgAdmin is a GUI tool used to manage PostgreSQL databases.

Using pgAdmin, we can:

1. Create databases
2. Create tables
3. Execute SQL queries
4. Manage database objects
5. Manage users


NOTE:

MySQL Workbench → Mainly used for MySQL

pgAdmin → Mainly used for PostgreSQL


## DAY 2 – DATABASE CONCEPTS

1. WHAT IS DATA?

Data is a collection of raw facts and information.

Example:

Name = Mayuri
Age = 22
City = Pune


2. WHAT IS A DATABASE?

A database is an organized collection of data.

It is used to store, manage, retrieve and update data
easily.

Example:

A college database can contain:

Students
Teachers
Courses
Marks
Attendance


3. WHY DO WE NEED A DATABASE?

We need a database because it helps us to:

1. Store large amounts of data
2. Organize data
3. Retrieve data quickly
4. Update data easily
5. Delete unwanted data
6. Maintain data consistency
7. Provide data security


Example:

Instead of storing thousands of student records in
separate files, we can store them in a database.


**TYPES OF DATABASE


1. RELATIONAL DATABASE

A relational database stores data in tables.

Tables contain:

Rows → Records
Columns → Attributes


Example:

Student Table

ID     Name       Age
1      Mayuri     22
2      Amit       23


Examples:

MySQL
PostgreSQL
Oracle
SQL Server


2. NoSQL DATABASE

NoSQL means "Not Only SQL".

NoSQL databases are generally used for non-relational data
and flexible data structures.

They do not always store data in traditional rows and
columns.

Examples:

MongoDB
Cassandra
Redis
DynamoDB


Common types of NoSQL databases:

1. Document Database
2. Key-Value Database
3. Column-Family Database
4. Graph Database



## DBMS


1. WHAT IS DBMS?

DBMS stands for:

Database Management System


Definition:

DBMS is software used to create, store, manage, update
and retrieve data from a database.


Examples:

MySQL
PostgreSQL
Oracle


Main functions of DBMS:

1. Store data
2. Retrieve data
3. Update data
4. Delete data
5. Manage users
6. Provide security
7. Backup and recovery


***. TYPES OF DBMS

Main types of DBMS:

1. Hierarchical DBMS
2. Network DBMS
3. Relational DBMS
4. Object-Oriented DBMS


1. HIERARCHICAL DBMS

Data is organized in a tree-like structure.

It follows:

Parent → Child relationship


Example:

Company
 |
 |-- IT
 |    |-- Developer
 |    |-- Tester
 |
 |-- HR


2 NETWORK DBMS

Data is organized using a network structure.

A record can have multiple relationships.

It supports many-to-many relationships.


3 RELATIONAL DBMS

RDBMS stores data in tables.

Tables can be connected using relationships.

Examples:

MySQL
PostgreSQL
Oracle
SQL Server


### RDBMS

RDBMS stands for:

Relational Database Management System


Definition:

RDBMS is a type of DBMS that stores data in tables and
allows relationships between tables.


Example:

Student Table

Student_ID    Name
1             Mayuri
2             Amit


Course Table

Course_ID     Course_Name
101           SQL
102           Python


Tables can be related using keys.


### RDBMS VS NoSQL

** RDBMS:

1. Stores data mainly in tables
2. Uses rows and columns
3. Usually follows a defined schema
4. Commonly uses SQL
5. Supports relationships between tables
6. Uses keys such as Primary Key and Foreign Key
7. Good for structured data

Examples:

MySQL
PostgreSQL
Oracle
SQL Server


** NoSQL:

1. Does not require traditional relational tables
2. Has flexible data structures
3. Schema can be flexible
4. Query method depends on the NoSQL database
5. Suitable for large-scale and rapidly changing data
6. Commonly used for unstructured or semi-structured data

Examples:

MongoDB
Redis
Cassandra


### PRIMARY KEY VS FOREIGN KEY


** PRIMARY KEY

A Primary Key is a column or combination of columns that
uniquely identifies each record in a table.

Rules:

1. Values must be unique
2. NULL values are not allowed
3. A table can have only one PRIMARY KEY constraint
4. Primary Key can contain one or more columns


Example:

CREATE TABLE student (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(50)
);


student_id

1
2
3

Each ID is unique.


** FOREIGN KEY

A Foreign Key is a column that creates a relationship
between two tables.

It references a key in another table, commonly the Primary
Key.


Example:

CREATE TABLE department (
    department_id INT PRIMARY KEY,
    department_name VARCHAR(50)
);


CREATE TABLE employee (
    employee_id INT PRIMARY KEY,
    employee_name VARCHAR(50),
    department_id INT,
    FOREIGN KEY (department_id)
    REFERENCES department(department_id)
);


Here:

department_id in department table
→ PRIMARY KEY

department_id in employee table
→ FOREIGN KEY


WHAT IS SQL?

SQL stands for:

Structured Query Language


Definition:

SQL is a language used to communicate with and manage data
stored in relational databases.


Using SQL, we can:

1. Create databases
2. Create tables
3. Insert data
4. Read data
5. Update data
6. Delete data
7. Search and filter data


Example:

SELECT * FROM student;


### TYPES OF SQL COMMANDS

SQL commands are mainly divided into:

1. DDL
2. DML
3. DQL
4. DCL
5. TCL


1. DDL – Data Definition Language

DDL is used to define and modify the structure of database
objects such as tables.

Commands:

CREATE
ALTER
DROP
TRUNCATE


Example:

CREATE TABLE student (
    id INT,
    name VARCHAR(50)
);


ALTER TABLE student ADD age INT;


DROP TABLE student;


TRUNCATE TABLE student;


2. DML – Data Manipulation Language

DML is used to add, modify and remove data from tables.

Commands:

INSERT
UPDATE
DELETE


Example:

INSERT INTO student VALUES (1, 'Mayuri');


UPDATE student
SET name = 'Amit'
WHERE id = 1;


DELETE FROM student
WHERE id = 1;


3. DQL – Data Query Language

DQL is used to retrieve data from a table.

Command:

SELECT


Example:

SELECT * FROM student;

SELECT name FROM student;


4. DCL – Data Control Language

DCL is used to control access and permissions in a database.

Commands:

GRANT
REVOKE


GRANT → Gives permission

REVOKE → Removes permission


5. TCL – Transaction Control Language

TCL is used to manage transactions.

Commands:

COMMIT
ROLLBACK
SAVEPOINT


COMMIT → Saves transaction changes permanently.

ROLLBACK → Undoes transaction changes when supported.


### DAY 3 – SQL DATA TYPES



WHAT IS A DATA TYPE?

A data type defines what type of value can be stored in a
column.

Example:

Age → INT
Name → VARCHAR
Date of Birth → DATE
Salary → DECIMAL


Why do we use data types?

1. To define the type of data
2. To control what values can be stored
3. To use storage efficiently
4. To maintain data accuracy



1. INT

INT stands for Integer.

It is used to store whole numbers.

Examples:

10
100
500
-20


Example:

age INT;


Rules:

1. Stores whole numbers
2. Does not store decimal values
3. Can store positive and negative values


Example:

CREATE TABLE student (
    age INT
);


2. VARCHAR

VARCHAR stands for Variable Character.

It is used to store text/string values of variable length.


Syntax:

VARCHAR(n)


Example:

name VARCHAR(50);


Examples:

'Mayuri'
'Rahul'
'Pune'


VARCHAR(50) means the maximum length is 50 characters.


3. CHAR

CHAR is used to store fixed-length character/string data.


Syntax:

CHAR(n)


Example:

gender CHAR(1);


Values:

'M'
'F'


Difference:

CHAR → Fixed-length character data

VARCHAR → Variable-length character data


4. BIGINT

BIGINT is used to store very large whole numbers.

Example:

employee_id BIGINT;


Example value:

9876543210


Use BIGINT when the number may be larger than the range
normally required for INT.


5. TINYINT

TINYINT is used to store small whole numbers.

Example:

age TINYINT;


Common uses:

Age
Small counters
Status values


Example:

age TINYINT;


Values:

18
22
30
45


6. DECIMAL


DECIMAL is used to store exact decimal numbers.

Common uses:

Salary
Price
Amount
Financial data


Syntax:

DECIMAL(M,D)


M = Total number of digits

D = Number of digits after decimal point


Example:

salary DECIMAL(10,2);


Example values:

25000.50
1500.75
99999.99


DECIMAL(10,2) means:

Total digits = 10
Digits after decimal point = 2

So up to 8 digits can be before the decimal point
(excluding sign).


IMPORTANT:

DECIMAL is preferred when exact decimal values are
important.


7. FLOAT

FLOAT is a floating-point numeric data type used to store
approximate decimal numbers.

Example:

temperature FLOAT;


Values:

25.5
36.7
98.6


IMPORTANT:

FLOAT stores approximate values.

It may not represent every decimal value exactly because
floating-point numbers use approximate binary representation.


Use:

FLOAT → Approximate / scientific measurements

DECIMAL → Exact values such as money and salary


Example:

temperature FLOAT;

salary DECIMAL(10,2);


8. DATE

DATE is used to store date values.

Format:

YYYY-MM-DD


Example:

2026-08-12


Example:

birth_date DATE;


DATE stores:

Year
Month
Day



9. YEAR


YEAR is used to store a year value.

Example:

birth_year YEAR;


Example values:

2000
2001
2020
2026


Use YEAR when only the year is required.


10. BOOLEAN


BOOLEAN is used to represent TRUE or FALSE values.

Example:

is_active BOOLEAN;


Values:

TRUE
FALSE


In MySQL, BOOLEAN is a synonym for TINYINT(1).

Common uses:

is_active
is_verified
is_available


11. BLOB

BLOB stands for:

Binary Large Object


BLOB is used to store binary data.

Examples:

Images
Files
Binary data


Example:

profile_image BLOB;


BLOB types in MySQL include:

TINYBLOB
BLOB
MEDIUMBLOB
LONGBLOB



*** DATA TYPES – QUICK REVISION

INT      → Whole number
BIGINT   → Large whole number
TINYINT  → Small whole number
VARCHAR  → Variable-length text
CHAR     → Fixed-length text
DECIMAL  → Exact decimal number
FLOAT    → Approximate decimal number
DATE     → Date
YEAR     → Year
BOOLEAN  → TRUE/FALSE
BLOB     → Binary data



### DAY 4 – SQL CONSTRAINTS


WHAT IS A CONSTRAINT?

A constraint is a rule applied to a column or table to
control the data that can be stored.

Constraints help maintain data accuracy and data integrity.


Common SQL constraints:

1. PRIMARY KEY
2. NOT NULL
3. FOREIGN KEY
4. DEFAULT
5. CHECK
6. UNIQUE



1. PRIMARY KEY CONSTRAINT

Primary Key uniquely identifies each record in a table.

Rules:

1. Values must be unique
2. NULL values are not allowed
3. A table can have only one PRIMARY KEY constraint
4. Primary Key can contain one or more columns


Example:

CREATE TABLE student (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(50)
);


2. NOT NULL

NOT NULL means a column cannot contain NULL values.

Example:

CREATE TABLE student (
    student_id INT,
    student_name VARCHAR(50) NOT NULL
);


Valid:

INSERT INTO student
VALUES (1, 'Mayuri');


Invalid:

INSERT INTO student
VALUES (2, NULL);


3. FOREIGN KEY

FOREIGN KEY is used to create a relationship between two
tables.

It references a key in another table, commonly the Primary
Key.


Example:

CREATE TABLE department (
    department_id INT PRIMARY KEY,
    department_name VARCHAR(50)
);


CREATE TABLE employee (
    employee_id INT PRIMARY KEY,
    employee_name VARCHAR(50),
    department_id INT,

    FOREIGN KEY (department_id)
    REFERENCES department(department_id)
);



4. DEFAULT


DEFAULT provides an automatic value when a value is not
specified for a column during INSERT.


Example:

CREATE TABLE employee (
    id INT,
    name VARCHAR(50),
    city VARCHAR(50) DEFAULT 'Pune'
);


Insert:

INSERT INTO employee (id, name)
VALUES (1, 'Mayuri');


If city is not provided, the default value will be:

Pune


5. CHECK


CHECK constraint is used to restrict the values that can be
stored in a column according to a condition.


Example:

CREATE TABLE student (
    id INT,
    age INT CHECK (age >= 18)
);


Here:

age must be greater than or equal to 18.


Valid:

INSERT INTO student
VALUES (1, 22);


Invalid:

INSERT INTO student
VALUES (2, 15);


15 is invalid because:

15 < 18


Another example:

CREATE TABLE employee (
    id INT,
    salary DECIMAL(10,2) CHECK (salary > 0)
);


Here:

Salary must be greater than 0.


IMPORTANT:

CHECK is used to validate data based on a condition.

Examples:

age >= 18
salary > 0
marks BETWEEN 0 AND 100



6. UNIQUE


UNIQUE constraint ensures that duplicate values are not
allowed in a column.


Example:

CREATE TABLE student (
    id INT PRIMARY KEY,
    email VARCHAR(100) UNIQUE
);


Two rows cannot have the same email value.



### CONSTRAINTS – QUICK REVISION


PRIMARY KEY → Uniquely identifies each record

NOT NULL     → NULL value is not allowed

FOREIGN KEY  → Creates relationship between tables

DEFAULT      → Provides an automatic default value

CHECK        → Allows values according to a condition

UNIQUE       → Prevents duplic