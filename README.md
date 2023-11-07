# EX-3-SubQueries-Views-and-Joins
## DATE : 17/8/2023
## AIM:
TO read and write SubQueries-Views-and-Joins.
## STEP1:
Create a new database.
## STEP2:
Use the newly created database.
## STEP3:
A database called "employee_management" is created, and two tables, "departments" and "employees," are defined. Sample data is inserted into these tables.
## STEP4:
A view called "employee_departments" is created to display employees and their corresponding departments using a LEFT JOIN between the "employees" and "departments" tables
## STEP5:
The LEFT JOIN is used to retrieve all employees and their departments, including employees who do not belong to any department.
A RIGHT JOIN is used to retrieve all departments and their employees, including departments without any employees. In this case, it leverages the previously created view "employee_departments" to perform the join.
## STEP6:
Drop the "employee_management" database .
# OUTPUT:
### SubQueries-Views-and-Joins:
#### QUERY:
Create tables for employees and departments.
```
CREATE TABLE departments (
    department_id INT AUTO_INCREMENT PRIMARY KEY,
    department_name VARCHAR(255)
);
```
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/9057193a-2308-49b2-b461-437942b70f7a)
```
CREATE TABLE employees (
    employee_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(255),
    last_name VARCHAR(255),
    department_id INT,
   salary DECIMAL(10, 2),
   FOREIGN KEY (department_id) REFERENCES departments(department_id) );
```
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/4b2cc3b0-ead3-4c45-9aa5-931dabecc95c)


#### QUERY:
Insert sample data into the tables.
```
INSERT INTO departments (department_name) VALUES
    ('HR'),
    ('Finance'),
    ('IT');
```
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/c9fe5b00-a234-4cc6-8d04-4027468ae541)
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/2b102a5f-7388-409b-8adf-9a205309b9e1)
```
INSERT INTO employees (first_name, last_name, department_id, salary) VALUES
    ('John', 'Doe', 1, 60000.00),
    ('Jane', 'Smith', 1, 55000.00),
    ('David', 'Johnson', 2, 75000.00),
    ('Emily', 'Brown', 3, 80000.00);
```
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/6d13c1de-bf6b-4150-8086-bb9d83b47205)
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/5ceb2350-3184-4385-b7a5-65c3e9d2d7ec)


#### QUERY:
Create a view to display employees and their departments.
```
CREATE VIEW employee_departments AS
SELECT
    e.employee_id,
    e.first_name,
    e.last_name,
    d.department_name,
    e.salary
FROM
    employees e
LEFT JOIN
    departments d ON e.department_id = d.department_id;
```
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/f88dcf2d-000a-4d78-926b-6c417e67b1db)

##### Use a LEFT JOIN to retrieve all employees and their departments:
```
SELECT * FROM employee_departments;
```
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/74e3c647-eee0-4580-b626-eab3e1b23338)

##### Use a RIGHT JOIN to retrieve all departments and their employees:
```
SELECT * FROM employee_departments e
RIGHT JOIN departments d ON e.department_name = d.department_name;
```
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/882c9a53-7a36-4264-a0fe-f5a94581f25e)
##### DROP DATABASE :
```
DROP DATABASE employee_management;
```
![image](https://github.com/Jeevithaelumalai/EX-3-SubQueries-Views-and-Joins/assets/118708245/96b11498-e616-4821-bb5a-2f0f44a3b116)

# RESULT:
Thus the all the queries got the output and statifies the given question.



