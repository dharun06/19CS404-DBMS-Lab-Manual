# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
-- Paste Question 1 here

```sql
update Employees set FIRST_NAME = 'John' WHERE DEPARTMENT_ID=80 AND COMMISSION_PCT<.35;
```

**Output:**

![Output1](output.png)

**Question 2**
---
-- Paste Question 2 here

```sql
UPDATE Employees set EMAIL ='Unavailable';
```

**Output:**

![Output2](output.png)

**Question 3**
---
-- Paste Question 3 here

```sql
delete from Customer WHERE GRADE%2 = 1;
```

**Output:**

![Output3](output.png)

**Question 4**
---
-- Paste Question 4 here

```sql
delete from Customer where GRADE>=2;
```

**Output:**

![Output4](output.png)

**Question 5**
---
-- Paste Question 5 here

```sql
SELECT * FROM EmployeeInfo where EmpFname like 'S%';
```

**Output:**

![Output5](output.png)

**Question 6**
---
-- Paste Question 6 here

```sql
select * from EmployeeInfo where EmpID >=5 and EmpID < 10;
```

**Output:**

![Output6](output.png)

**Question 7**
---
-- Paste Question 7 here

```sql
select * from customer where city = 'New York' or grade = 100;
```

**Output:**

![Output7](output.png)

**Question 8**
---
-- Paste Question 8 here

```sql
select id,value1, ABS(value1) as 'absolute_value' from Calculations;
```

**Output:**

![Output8](output.png)

**Question 9**
---
-- Paste Question 9 here

```sql
select dname || ', ' || loc as 'dept_location' from dept;
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
update product set per_unit_price = 25 where purchase_date = '2022-08-15' and product_id = 12; 
```

**Output:**

![Output10](output.png)

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
