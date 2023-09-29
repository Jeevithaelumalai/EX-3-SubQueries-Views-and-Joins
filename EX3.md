# EX 3 SubQueries, Views and Joins 


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
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/76257329-c37b-45c6-b566-08cf46bb569b)


### OUTPUT:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/a6630307-26bc-486c-9957-11228cde4358)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/051cd728-83e2-42eb-a92e-53813cd6a11f)


### OUTPUT:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/c760b2a2-d01a-4eb5-ba58-0efe5234266d)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/1748ae78-d501-4e2b-8d66-999567cbd752)


### OUTPUT:

![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/fd8d7622-04c1-4465-b4b6-a13b518541a8)

### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/902aa3e7-c3db-4903-81a5-c998e2b380af)


### OUTPUT:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/d616d8c1-4a0a-45b9-9c3e-3237aa8a30fe)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/bd45fac3-0c35-4cf4-ab5d-e20873a282d3)


### OUTPUT:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/e5b5e999-d264-4c29-aedd-166ce583d0df)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:

![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/2265aee4-55ef-421f-be72-deb9384bb204)

### OUTPUT:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/2d3e7482-4adf-48ae-96aa-3c3aa032ff11)

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
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/8c0e1a09-1c8a-43de-9fb0-96a8cbe82c31)


### OUTPUT:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/6b8c6a1c-bf98-419b-8ec6-2abe198596f8)


### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/6d4b1a7b-255f-45d7-8ed3-5c66954eed94)


### OUTPUT:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/408a2fac-87d5-4561-90e8-7c12cbe7d4a5)

### Q9) Perform Natural join on both tables

### QUERY:

![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/ec16d2d1-8657-4d0f-98c0-71667c3bd6a7)
### OUTPUT:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/8745edec-7338-4d22-8621-a4bea2bd3b5b)
### Q10) Perform Left and right join on both tables
### QUERY:
#### Left Join:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/b1878d47-e271-48ea-bf85-9ce7a6c3b686)
####Right Join:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/a61c87fd-745b-4e7b-b9cb-ab9af97fa300)



### OUTPUT:
#### Left Join:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/0bd19bfe-ce5d-4edb-8bda-e99baeeed654)

#### RIGHT Join:
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/4a288f12-60ab-42a7-bef3-b825fb86db3c)

