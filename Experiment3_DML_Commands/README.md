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
-- ![image](https://github.com/user-attachments/assets/c8ed2c96-971a-4afa-8aef-6ceaa8ee73aa)


```sql
-- update PRODUCTS set reorder_lvl=40 where category='Grocery';
```

**Output:**

![image](https://github.com/user-attachments/assets/8fc512c5-3539-4a51-86cb-98a52d113cb3)


**Question 2**
---
-- ![image](https://github.com/user-attachments/assets/ff56cb5d-2aa7-4324-a928-17d99a92fe0a)


```sql
-- update Products set sell_price=sell_price*1.15 where quantity<50 and supplier_id=10;
```

**Output:**

![image](https://github.com/user-attachments/assets/205e43f4-b346-4cc8-812f-2daa44ff44ce)


**Question 3**
---
-- ![image](https://github.com/user-attachments/assets/61076362-5534-4f85-8a68-97e57aa54527)


```sql
-- update products set reorder_lvl=reorder_lvl*1.30 where category='Food' and quantity<(reorder_lvl*0.5) ;
```

**Output:**

![image](https://github.com/user-attachments/assets/36808404-880d-46a7-aa00-f5f3c6bc418c)


**Question 4**
---
-- ![image](https://github.com/user-attachments/assets/db61b07a-5fb0-4c9d-8abd-1b576723145c)


```sql
-- update Products set quantity=quantity*1.10;
```

**Output:**

![image](https://github.com/user-attachments/assets/adf7e262-d139-4227-ac46-8d0e6503e8fa)


**Question 5**
---
-- ![image](https://github.com/user-attachments/assets/b2bc4d0c-a266-4de0-af7b-0cbd4c447d33)


```sql
-- update Products set reorder_lvl=20 where quantity<10 and category='Snacks';
```

**Output:**

![image](https://github.com/user-attachments/assets/500c4db6-b435-4bd2-aa43-280d513f7929)


**Question 6**
---
-- ![image](https://github.com/user-attachments/assets/8d631881-9048-4c23-845f-5447d904770f)


```sql
-- delete from Customer where WORKING_AREA='New York';
```

**Output:**

![image](https://github.com/user-attachments/assets/e452fb49-d3d7-4643-8620-0d7a07be37bc)


**Question 7**
---
-- ![image](https://github.com/user-attachments/assets/2dc1d0ab-9dea-4ac0-a94e-3856e0b55769)


```sql
-- delete from Customer where GRADE=3 and CUST_NAME like '%BBB%' and PAYMENT_AMT >2000;
```

**Output:**

![image](https://github.com/user-attachments/assets/072f101d-5a43-49af-8518-8af10322e8c6)


**Question 8**
---
-- ![image](https://github.com/user-attachments/assets/37796a55-a562-4354-8e38-44955d2763ce)


```sql
-- delete from Customer where OPENING_AMT between 4000 and 6000;
```

**Output:**

![image](https://github.com/user-attachments/assets/6e5cd051-40ac-43ff-8f53-d543cc02d9ec)


**Question 9**
---
-- ![image](https://github.com/user-attachments/assets/358305df-06be-42aa-9cf8-df85dd8cbc4e)

```sql
-- delete from Customer where CUST_CITY <> 'New York' and OUTSTANDING_AMT>5000;
```

**Output:**

![image](https://github.com/user-attachments/assets/e32c1d1d-28d4-411f-85e8-3488d78806c5)


**Question 10**
---
-- ![image](https://github.com/user-attachments/assets/80bec1b7-c573-405e-a4f1-7c866508b665)


```sql
-- delete from Customer where (GRADE=3 or AGENT_CODE='A008') and OUTSTANDING_AMT<5000;
```

**Output:**

![image](https://github.com/user-attachments/assets/21f4db31-cb75-4d9c-afcf-41fe3dadc2d7)


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
