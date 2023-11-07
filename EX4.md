# Ex. No: 4 Creating Procedures using PL/SQL

DATE : 25.09.2023

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
CREATE TABLE employee6( empid NUMBER,empname VARCHAR(10),dept VARCHAR(10), salary NUMBER);
 set serveroutput on
SQL> CREATE OR REPLACE PROCEDURE emp_data AS
  2  BEGIN
  3  INSERT INTO employee6(empid,empname,dept,salary)
  4   values(1,'jerry','Manager',1500000);
  5  INSERT INTO employee6(empid,empname,dept,salary)
  6   values(2,'harry','ceo',5000000);
  7  INSERT INTO employee6(empid,empname,dept,salary)
  8   values(1,'tom','clerk',15000);
  9   COMMIT;
 10   FOR emp_rec IN (SELECT * FROM employee6)LOOP
 11  DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
 12  END LOOP;
 13  END;
 14   / 
```

### Output:
![dbms 4 op1](https://github.com/AtchayaSundaramoorthy/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119393516/101447f9-8253-4c02-9ed5-5720e94ad525)

![dbms 4 op2](https://github.com/AtchayaSundaramoorthy/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119393516/cb4729ba-5474-492e-a860-aa1c1ad972f3)


### Result:
THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY
