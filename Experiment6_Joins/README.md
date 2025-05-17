# Experiment 6: Joins

## AIM
To study and implement different types of joins.

## THEORY

SQL Joins are used to combine records from two or more tables based on a related column.

### 1. INNER JOIN
Returns records with matching values in both tables.

**Syntax:**
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

### 2. LEFT JOIN
Returns all records from the left table, and matched records from the right.

**Syntax:**

```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;
```
### 3. RIGHT JOIN
Returns all records from the right table, and matched records from the left.

**Syntax:**

```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;
```
### 4. FULL OUTER JOIN
Returns all records when there is a match in either left or right table.

**Syntax:**

```sql
SELECT columns
FROM table1
FULL OUTER JOIN table2
ON table1.column = table2.column;
```

**Question 1**
--
-- ![image](https://github.com/user-attachments/assets/008903bc-98be-4c48-a96b-17a15b988c57)


```sql
-- select p.* from PATIENTS p inner join APPOINTMENTS a
on p.patient_id=a.patient_id
where a.appointment_date between '2024-01-01' and '2024-01-31';
```

**Output:**

![image](https://github.com/user-attachments/assets/326a560b-92df-49ab-b9ef-5a147fd2e14e)


**Question 2**
---
-- ![image](https://github.com/user-attachments/assets/bf2d48a5-2de4-4689-bac5-3d7de9e4cb7f)


```sql
-- select c.cust_name as 'Customer Name' ,c.city,s.name as Salesman,s.city,s.commission
from customer c inner join salesman s
on c.salesman_id=s.salesman_id
where c.city<>s.city and s.commission>0.12;
```

**Output:**

![image](https://github.com/user-attachments/assets/4b03e5d9-99b2-4f3a-8f5e-02f92d5c8390)


**Question 3**
---
-- ![image](https://github.com/user-attachments/assets/33b209e2-bf68-410e-bf2f-88c6c812178e)


```sql
-- select c.cust_name,c.city,c.grade,s.name as Salesman,s.city 
from customer c inner join salesman s
on c.salesman_id=s.salesman_id
where c.grade<300
order by c.customer_id asc;
```

**Output:**

![image](https://github.com/user-attachments/assets/f99981dd-4664-4086-a98f-c7a3d171b34c)


**Question 4**
---
-- ![image](https://github.com/user-attachments/assets/9ec01c29-5048-4a5e-b812-ae4251a50bbc)


```sql
-- select c.cust_name,c.city,o.ord_no,o.ord_date,o.purch_amt as 'Order Amount' 
from customer c left outer join orders o 
on c.customer_id=o.customer_id
order by o.ord_date asc;
```

**Output:**

![image](https://github.com/user-attachments/assets/18a0b129-8cf1-483d-b5ef-4d8f79a59a84)


**Question 5**
---
-- ![image](https://github.com/user-attachments/assets/021cffa6-33f5-4979-be60-98dd99b86a5d)


```sql
-- Pselect c.cust_name,o.ord_no,o.ord_date,o.purch_amt 
from CUSTOMER c left join ORDERS o
on c.customer_id=o.customer_id
where o.purch_amt>1000;
```

**Output:**

![image](https://github.com/user-attachments/assets/8ac207d0-ae4e-4faf-ac9d-6c018dbb2464)


**Question 6**
---
-- ![image](https://github.com/user-attachments/assets/fe5ff67e-a160-4757-b126-24bd962faa00)


```sql
-- select c.cust_name as 'Customer Name',c.city,s.name as Salesman,s.commission
from customer c inner join salesman s
on c.salesman_id=s.salesman_id;
```

**Output:**

![image](https://github.com/user-attachments/assets/65473555-1331-4cf6-a242-8087861bfdf2)


**Question 7**
---
-- ![image](https://github.com/user-attachments/assets/a815691c-9305-43b9-bde9-ccd65f4a99ad)


```sql
-- select s.name,c.cust_name,c.city,c.grade,c.salesman_id
from salesman s left join Customer c
on c.salesman_id=s.salesman_id;
```

**Output:**

![image](https://github.com/user-attachments/assets/7716a843-8130-410e-843f-d614593e4cb7)


**Question 8**
---
-- ![image](https://github.com/user-attachments/assets/e37ce53d-68e4-468d-9fcf-e10477511f75)


```sql
-- select p.first_name as patient_name, d.first_name as doctor_name 
from PATIENTS p inner join DOCTORS d
on p.doctor_id=d.doctor_id
where p.discharge_date not null;
```

**Output:**

![image](https://github.com/user-attachments/assets/490f825a-89bc-4e39-b927-5ea707d0aba6)


**Question 9**
---
-- ![image](https://github.com/user-attachments/assets/4fe16d56-b85c-466c-b8d8-5830a2c78fec)


```sql
-- select o.ord_no,o.purch_amt,c.cust_name,c.city 
from orders o inner join customer c
on o.customer_id=c.customer_id
where o.purch_amt  between 500 and 2000;
```

**Output:**

![image](https://github.com/user-attachments/assets/46887189-eb4a-4b3e-92e0-16d8f8a71ac0)


**Question 10**
---
-- ![image](https://github.com/user-attachments/assets/0f320dbf-9ef7-44b8-9883-a2e2eed0488c)


```sql
-- select p.first_name as patient_name, d.first_name as doctor_name 
from PATIENTS p inner join DOCTORS d
on p.doctor_id=d.doctor_id
where p.discharge_date is NULL;
```

**Output:**

![image](https://github.com/user-attachments/assets/612e7265-afe6-4f91-9fcc-414de73995fa)



## RESULT
Thus, the SQL queries to implement different types of joins have been executed successfully.
