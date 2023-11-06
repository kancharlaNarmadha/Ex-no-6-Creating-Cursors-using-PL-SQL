# Ex-no-6-Creating-Cursors-using-PL-SQL
# DATE:
# AIM:
To create a cursor using PL/SQL.
# Steps:
1.Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);

2.Create a cursor named as employee_cursor

3.Using cursor read each record and display the result

4.Close the cursor
# Program:
# Create employee table
```
create table employee1(empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
```
```
   set serveroutput on;
   declare
   cursor employee6_cursor is
   select EMPID,EMPNAME,DEPT,SALARY
   from employee6;
   emp_id number;
   emp_name varchar(50);
   emp_dept varchar(10);
   emp_salary number;
   begin
   open employee6_cursor;
   loop
   fetch employee6_cursor into emp_id,emp_name,emp_dept,emp_salary;
   exit when employee6_cursor%NOTFOUND;
   dbms_output.put_line('EMPLOYEE ID: ' || emp_id);
   dbms_output.put_line('EMPLOYEE NAME: ' || emp_name);
   dbms_output.put_line('DEPARTMENT: ' || emp_dept);
   dbms_output.put_line('SALARY ' || emp_salary);
   dbms_output.put_line('----------------------');
   END LOOP;
   close employee6_cursor;
   end;
   /
```
# Output:
# Employee table
![dbms exp 5 1](https://github.com/kancharlaNarmadha/Ex-no-6-Creating-Cursors-using-PL-SQL/assets/119559316/0ae4c904-0b05-4f26-baee-64a0d1747b9d)
# Cursor using PL/SQL:
![dmbs exp 6](https://github.com/kancharlaNarmadha/Ex-no-6-Creating-Cursors-using-PL-SQL/assets/119559316/789f899f-861a-4e99-b3c6-79a6c499224a)
# Result:
Thus a cursor is created using PL/SQL successfully.
