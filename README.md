# Ex-no-6-Creating-Cursors-using-PL-SQL
# AIM 
To create a cursor using PL/SQL.
# STEPS
1)Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER); 2)Create a cursor named as employee_cursor 3)Using cursor read each record and display the result 4)Close the cursor.
# PROGRAM
CREATE A TABLE FOR EMPLOYEE:
~~~
CREATE TABLE kira (emp_id number,emp_name char(20),emp_dept char(20),emp_salary number);
~~~
ISERTING THE VALUES:
~~~
INSERT INTO kira VALUES (1, 'praneetha', 'Sales', 50000);
INSERT INTO kira VALUES (1, 'nikitha', 'marketing', 60000);
INSERT INTO kira VALUES (3, 'harshini', 'Manager', 70000);
~~~
DECLARE CURSOR:
~~~
DECLARE
CURSOR kira_cursor IS
SELECT emp_id,emp_name,emp_dept,emp_salary
FROM kira;
emp_id NUMBER;
emp_name CHAR(50);
emp_dept CHAR(50);
emp_salary NUMBER;
BEGIN
OPEN kira_cursor;
~~~
FETCH AND DISPLAY THE RECORD:
~~~
LOOP
FETCH kira_cursor INTO emp_id, emp_name, emp_dept, emp_salary;
EXIT WHEN kira_cursor%NOTFOUND;
~~~
DISPLAY THE RESULT FOR EACH EMPLOYEE:
~~~
DBMS_OUTPUT.PUT_LINE('Employee ID: ' || emp_id);
DBMS_OUTPUT.PUT_LINE('Employee Name: ' || emp_name);
DBMS_OUTPUT.PUT_LINE('Department: ' || emp_dept);
DBMS_OUTPUT.PUT_LINE('Salary: ' || emp_salary);
END LOOP;
~~~
CLOSE THE CURSOR:
~~~
CLOSE kira_cursor;
END;
/
~~~
# OUTPUT
CREATE A TABLE FOR EMPLOYEE:
![3](https://github.com/21005984/Ex-no-6-Creating-Cursors-using-PL-SQL/assets/94748389/e84a0cba-25da-43f7-a7ef-184905001dcf)
ISERTING THE VALUES:
![1](https://github.com/21005984/Ex-no-6-Creating-Cursors-using-PL-SQL/assets/94748389/d4a8a43e-21ae-4f9d-9a18-42e77144119a)
![2](https://github.com/21005984/Ex-no-6-Creating-Cursors-using-PL-SQL/assets/94748389/614eab60-e787-4ff2-8445-26d3448c57ad)
DECLARE CURSOR:
![image](https://github.com/21005984/Ex-no-6-Creating-Cursors-using-PL-SQL/assets/94748389/4e559700-ed56-4d26-a47f-bd34c652b07c)
DISPLAY THE RESULT FOR EACH EMPLOYEE:
![image](https://github.com/21005984/Ex-no-6-Creating-Cursors-using-PL-SQL/assets/94748389/c732c4e8-6251-4c31-b3c1-1cad4f8d9172)

#RESULT:
Creating a cursor using SQL/PL has been executed successfully..








