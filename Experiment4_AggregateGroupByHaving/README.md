# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
-- Paste Question 1 here

```sql
select DoctorID, count(*) as TotalRecords from MedicalRecords group by DoctorID;
```

**Output:**

![Output1](output.png)

**Question 2**
---
-- Paste Question 2 here

```sql
select Specialty, count(*) as TotalDocto from Doctors group by specialty;
```

**Output:**

![Output2](output.png)

**Question 3**
---
-- Paste Question 3 here

```sql
select max(price) - min(price) as price_diff from fruits;
```

**Output:**

![Output3](output.png)

**Question 4**
---
-- Paste Question 4 here

```sql
select min(purch_amt) as MINIMUM from orders;
```

**Output:**

![Output4](output.png)

**Question 5**
---
-- Paste Question 5 here

```sql
select name, length(name) as length from customer order by length(name) desc limit 1;
```

**Output:**

![Output5](output.png)

**Question 6**
---
-- Paste Question 6 here

```sql
select name,email, length(email) as min_email_length from customer group by length(email) limit 1;
```

**Output:**

![Output6](output.png)

**Question 7**
---
-- Paste Question 7 here

```sql
select occupation, MIN(workhour) from employee1 group by occupation having MIN(workhour) > 8;
```

**Output:**

![Output7](output.png)

**Question 8**
---
-- Paste Question 8 here

```sql
select city, AVG(income) from employee group by city having avg(income) > 500000;
```

**Output:**

![Output8](output.png)

**Question 9**
---
-- Paste Question 9 here

```sql
select category_id, product_name, max(price) as Price from products group by category_id having max(price) > 15;
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
select InsuranceCompany, count(PatientID) as TotalPatients from Insurance group by InsuranceCompany;
```

**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
