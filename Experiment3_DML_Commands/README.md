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
-- ![image](https://github.com/user-attachments/assets/da398e73-f5a5-4208-82f3-af13ecac6bf9)


```sql
-- select Frequency, count(*) as
TotalPrescriptions
from Prescriptions
group by Frequency;
```

**Output:**

![image](https://github.com/user-attachments/assets/2333085f-ef5a-488b-a6ae-8a9680066c53)


**Question 2**
---
-- ![image](https://github.com/user-attachments/assets/70eda5b4-92bb-4e65-a874-3f65e2ceb366)


```sql
--select Specialty,Gender,count(*) as
TotalDoctors
from Doctors
group by Specialty,Gender;
```

**Output:**

![image](https://github.com/user-attachments/assets/38e9fcad-ce81-4d20-ae61-b121ae8298bb)


**Question 3**
---
-- ![image](https://github.com/user-attachments/assets/96118ec6-067e-4bc9-ab63-2a34c6abda58)


```sql
-- select InsuranceCompany, count(distinct PatientID) as
TotalPatients
from Insurance
group by InsuranceCompany;
```

**Output:**

![image](https://github.com/user-attachments/assets/79ef665d-fd03-412b-903e-5f08d5c8dfa0)


**Question 4**
---
-- ![image](https://github.com/user-attachments/assets/cf5d53b4-8a56-4f3e-a0f9-b278483a9304)


```sql
-- select count(*) as
employees_count
from employee
where income >50000;
```

**Output:**

![image](https://github.com/user-attachments/assets/4f95afd9-7791-4e3d-9b3a-4d22ebc9adc8)


**Question 5**
---
-- ![image](https://github.com/user-attachments/assets/50bf1984-818e-4ef8-abde-07bd1e8cdddc)


```sql
-- select count(distinct salesman_id) as
COUNT
from orders;
```

**Output:**

![image](https://github.com/user-attachments/assets/ccbaabf1-f389-46b0-a817-0fe1a490d94e)


**Question 6**
---
-- ![image](https://github.com/user-attachments/assets/23eb269e-577c-4bc0-8add-0cfdac80cccf)


```sql
-- select count(*) as COUNT
from customer
where city='Noida';
```

**Output:**

![image](https://github.com/user-attachments/assets/ba1b4415-9d8e-4748-806a-894daeb82e79)


**Question 7**
---
-- ![image](https://github.com/user-attachments/assets/cabc5ed3-d895-48f3-a309-6a4a6ebb268a)


```sql
-- select AVG(income) as avg_income
from employee
where name like 'A%';
```

**Output:**

![image](https://github.com/user-attachments/assets/d0274477-8b3e-49d0-8ff7-4c96dc7f281d)


**Question 8**
---
-- ![image](https://github.com/user-attachments/assets/4c1c82cc-a5c2-4d17-b80c-9010d712d905)


```sql
-- select occupation, AVG(workhour)
from employee1
group by occupation
having AVG(workhour) between 10 and 12;
```

**Output:**

![image](https://github.com/user-attachments/assets/dc3555ea-898b-4169-bf46-788a4fcff268)


**Question 9**
---
-- ![Uploading image.png…]()


```sql
-- select jdate,SUM(workhour)
from employee1
group by jdate
having SUM(workhour)>40;
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
-- Paste your SQL code below for Question 10
```

**Output:**

![Output10](output.png)

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
