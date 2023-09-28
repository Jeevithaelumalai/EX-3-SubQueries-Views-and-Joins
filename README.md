# EX-3-SubQueries-Views-and-Joins
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
#### QUERY:
Insert sample data into the tables.
```
INSERT INTO departments (department_name) VALUES
    ('HR'),
    ('Finance'),
    ('IT');

INSERT INTO employees (first_name, last_name, department_id, salary) VALUES
    ('John', 'Doe', 1, 60000.00),
    ('Jane', 'Smith', 1, 55000.00),
    ('David', 'Johnson', 2, 75000.00),
    ('Emily', 'Brown', 3, 80000.00);
```
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
##### Use a LEFT JOIN to retrieve all employees and their departments:
```
SELECT * FROM employee_departments;
```
##### Use a RIGHT JOIN to retrieve all departments and their employees:
```
SELECT * FROM employee_departments e
RIGHT JOIN departments d ON e.department_name = d.department_name;
```
# RESULT:
Thus the all the queries got the output and statifies the given question.



