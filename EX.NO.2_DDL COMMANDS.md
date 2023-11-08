# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:
```sql
create database student_db;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/b5606517-63e6-4877-b573-5e0fbb9b3911)

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```sql
create table student(Regno int,Name varchar(20),Age int,Address varchar(50),Phonenumber varchar(10));
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/580dde75-4001-46da-8247-57d0cce15ee0)

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```sql
alter table student
add dept varchar(20);
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/2d6305f7-7009-454c-8f7f-10cf062de721)

### 6) Rename the student table to mystudent 
 
### SQL QUERY: 
```sql
alter table student
rename to mystudent;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/2e1493d7-eba9-4900-bb5f-1f0b1b537d4c)

### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```sql
truncate table student;
```
### OUTPUT:

### 6) Drop the mystudent table

### SQL QUERY: 
```sql
drop table student;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/447a97f8-16cf-4ca9-add7-3cbd2fa8611e)









## Result:
         Thus the basic DDL commands in SQL are executed. 


