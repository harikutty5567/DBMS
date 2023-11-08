# EX.NO.5 SubQueries, Views and Joins 
### DATE
## AIM
### To use SubQueries, Views and Joins in SQL 
## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/967f9341-a962-4fd5-9a69-ee09e1189ec3)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/fb10851d-74bd-4d8e-b053-ca5f82d93505)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/20a92860-c04e-429f-8e18-6bff8bf66008)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/193fe8e0-4929-4254-bad8-8a20db792ca9)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/bcbb58d8-a161-4fdb-a634-c297bf6a0109)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/cb8433ff-e3e0-4c0a-80b5-adb310213f8d)

### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/3059cd21-7496-4a29-ad19-d69762d5c256)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/a82e4a36-0372-4606-8303-bb62a77c7364)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/fdd8e006-7395-43ce-8845-d518c940d6c7)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/b2a9202b-0d4f-46fb-8694-4ee8ea9eb019)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/5da05b35-5a67-4190-82d3-424351a20169)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/94200b50-8997-45b9-80b6-048bd23b1b60)

## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/ce46e426-f49a-41bc-86d6-b12eb4eb925b)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/295ed344-215a-4202-bce4-2ced64433a73)

### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/74324a77-4d0d-4cc7-a65f-931a1ab27bde)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/ffca5512-0ca4-4334-90fc-483610988f86)

### Q9) Perform Natural join on both tables

### QUERY:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/471ddb5a-e6e2-4c16-a36c-3e3188ef3c2e)

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/be690aa7-804d-4ede-acf6-8272c8962325)

### Q10) Perform Left and right join on both tables

### QUERY:

## Left join
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/dd047c77-f913-4d11-ac15-d84fec5d34d7)

## Right join
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/6e4a2341-28c9-4711-b563-58d60d21606a)

### OUTPUT:

## Left join
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/3cbd6283-b5b8-4733-b138-40fd387eba35)

## Right join
![image](https://github.com/DrUmaRaniV/DBMS/assets/148323123/ec786e3f-695b-41fb-9f35-0e884b2db4fe)

## RESULT 
### Thus the basics of subqueries,views,joins are performed in SQL.
