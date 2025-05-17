# Experiment 5: Subqueries and Views

## AIM
To study and implement subqueries and views.

## THEORY

### Subqueries
A subquery is a query inside another SQL query and is embedded in:
- WHERE clause
- HAVING clause
- FROM clause

**Types:**
- **Single-row subquery**:
  Sub queries can also return more than one value. Such results should be made use along with the operators in and any.
- **Multiple-row subquery**:
  Here more than one subquery is used. These multiple sub queries are combined by means of ‘and’ & ‘or’ keywords.
- **Correlated subquery**:
  A subquery is evaluated once for the entire parent statement whereas a correlated Sub query is evaluated once per row processed by the parent statement.

**Example:**
```sql
SELECT * FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```
### Views
A view is a virtual table based on the result of an SQL SELECT query.
**Create View:**
```sql
CREATE VIEW view_name AS
SELECT column1, column2 FROM table_name WHERE condition;
```
**Drop View:**
```sql
DROP VIEW view_name;
```

**Question 1**
--
-- ![image](https://github.com/user-attachments/assets/442bd563-9801-40aa-9fa6-890df5e37a51)


```sql
-- SELECT student_name, grade
FROM GRADES
WHERE (subject, grade) IN (
    SELECT subject, MIN(grade)
    FROM GRADES
    GROUP BY subject
);
```

**Output:**

![image](https://github.com/user-attachments/assets/379fcd92-f7c5-432d-9768-3a749106f051)


**Question 2**
---
-- ![image](https://github.com/user-attachments/assets/8c682fc0-7bc5-4bef-b693-f9b2e8132152)


```sql
-- SELECT *
FROM CUSTOMERS
WHERE AGE < 30;
```

**Output:**

![image](https://github.com/user-attachments/assets/1b12b471-c4b2-4b1a-954a-2bb39cd8ce6e)


**Question 3**
---
-- ![image](https://github.com/user-attachments/assets/0db89160-2892-4021-916e-bffab50812d6)


```sql
-- SELECT *
FROM Medications
WHERE dosage = (
    SELECT MIN(dosage)
    FROM Medications
);
```

**Output:**

![image](https://github.com/user-attachments/assets/c1626473-53ee-4cc0-ba1c-fc6e1998f78b)


**Question 4**
---
-- ![image](https://github.com/user-attachments/assets/60a9dd51-1352-4d9c-9d63-371deb6537f6)


```sql
-- SELECT *
FROM CUSTOMERS
WHERE SALARY > 1500;

```

**Output:**

![image](https://github.com/user-attachments/assets/3eff1a4c-7cef-4bff-900a-04986c75e40b)


**Question 5**
---
-- ![image](https://github.com/user-attachments/assets/09812872-9498-4541-92ee-9a0a422a3869)


```sql
-- SELECT *
FROM customer
WHERE customer_id = (
    SELECT (s.salesman_id - 2001)
    FROM salesman s
    WHERE s.name = 'Mc Lyon'
);

```

**Output:**

![image](https://github.com/user-attachments/assets/05f9f4cd-c63e-477b-865a-b562efc4f80f)


**Question 6**
---
-- ![image](https://github.com/user-attachments/assets/b43fdf96-feed-4630-8cc8-5fc6a22e5cc9)


```sql
-- SELECT *
FROM CUSTOMERS
WHERE SALARY < 2500;
```

**Output:**

![image](https://github.com/user-attachments/assets/bd2f6ab4-634d-496c-aa4d-2dfa49220605)


**Question 7**
---
-- ![image](https://github.com/user-attachments/assets/68418b73-c953-49ff-aefa-79cf7e33afd1)


```sql
-- SELECT *
FROM CUSTOMERS
WHERE ADDRESS = 'Delhi';
```

**Output:**

![image](https://github.com/user-attachments/assets/c48f9d71-e923-4141-ba1d-158942f30545)


**Question 8**
---
-- ![image](https://github.com/user-attachments/assets/e8e88ffc-e873-4623-8c9f-54ae8f9ca142)


```sql
-- SELECT name
FROM customer
WHERE phone NOT IN (
    SELECT phone
    FROM customer
    GROUP BY phone
    HAVING COUNT(phone) > 1
);
```

**Output:**

![image](https://github.com/user-attachments/assets/9201cbdd-7e3b-4871-baad-63ea191a4666)


**Question 9**
---
-- ![image](https://github.com/user-attachments/assets/e44a2306-a371-4ee5-aa0b-c670c72ea42b)


```sql
-- select  * from orders where salesman_id in (select salesman_id from salesman where name='Paul Adam');
```

**Output:**

![image](https://github.com/user-attachments/assets/42be4875-2eb4-40ec-9200-695e1271b020)


**Question 10**
---
-- ![image](https://github.com/user-attachments/assets/5399e750-d2d0-41ac-9ca7-b36b78350b25)


```sql
-- select * from Employee where age<(select avg(age) from Employee where income>1000000);
```

**Output:**

![image](https://github.com/user-attachments/assets/cbf2f68a-0875-45a3-b6bc-e310b31379c9)



## RESULT
Thus, the SQL queries to implement subqueries and views have been executed successfully.
