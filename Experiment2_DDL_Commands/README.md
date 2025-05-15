# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
--
![image](https://github.com/user-attachments/assets/a0a5dc65-aa14-4bc7-994e-1d87088595a9)


```sql
alter table Companies add designation varchar(50);
alter table Companies add net_salary  number;
```

**Output:**

![image](https://github.com/user-attachments/assets/505dee91-b4ee-472e-a541-4bae6b55c2f8)



**Question 2**
---
![image](https://github.com/user-attachments/assets/bd4392f0-6be0-48b9-b1ca-531e1bf69e38)


```sql
insert into Products(ProductID,Name,Category,Price,Stock) values(101,"Laptop","Electronics",1500,50);
```

**Output:**

![image](https://github.com/user-attachments/assets/ba1c5b7c-ab64-40aa-aaec-8842f204c76f)


**Question 3**
---
![image](https://github.com/user-attachments/assets/99977b71-1c8d-4b3a-b8f5-80b1699f336c)


```sql
create table Tasks(
TaskID INTEGER,
TaskName TEXT,
DueDate DATE
);
```

**Output:**

![image](https://github.com/user-attachments/assets/b182a3bd-2fae-4758-b0a8-d5646331f000)


**Question 4**
---
![image](https://github.com/user-attachments/assets/7663d7c4-38aa-4fa6-9005-2f095f9e37f9)


```sql
insert into Customers(CustomerID,Name,Address,City,ZipCode) values(302,"Laura Croft","456 Elm St","Seattle",98101);
insert into Customers(CustomerID,Name,Address,City,ZipCode) values(303,"Bruce Wayne","789 Oak St","Gotham",10001);
```

**Output:**
![image](https://github.com/user-attachments/assets/8828c730-1206-4736-904e-106412a9f87c)


**Question 5**
---
![image](https://github.com/user-attachments/assets/28cee191-46b3-445a-9cb3-671dd9d4f77b)


```sql
insert into Books(ISBN, Title, Author, Publisher, YearPublished) select ISBN, Title, Author, Publisher, YearPublished from Out_of_print_books;
```

**Output:**

![image](https://github.com/user-attachments/assets/b18cea2c-8dd1-49f7-9379-6e78f9ab9035)


**Question 6**
---
![image](https://github.com/user-attachments/assets/d4f27092-3f31-40b3-9105-72c23907f8b9)


```sql
create table Department(
DepartmentID INTEGER primary key,
DepartmentName TEXT  unique  not NULL,
Location  TEXT
);
```

**Output:**

![image](https://github.com/user-attachments/assets/2eb8ff67-0689-4ab4-b632-1d8ba21c7f03)


**Question 7**
---
![image](https://github.com/user-attachments/assets/a42531a1-c8b6-452f-a629-efc5dc76932a)


```sql
create table item(
item_id TEXT primary key,
item_desc TEXT,
rate INTEGER,
icom_id TEXT,
foreign key(icom_id) references company(com_id) on update set null on delete set null,
check(length(icom_id)=4)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/09e67f32-2f32-48c3-9469-3676167aac0a)


**Question 8**
---![image](https://github.com/user-attachments/assets/c32fe6c1-9480-4ab1-9542-9914ba605bc7)


```sql
create table item(
item_id TEXT primary key,
item_desc TEXT,
rate INTEGER,
icom_id TEXT,
foreign key(icom_id) references company(com_id) on update cascade on delete cascade,
check(length(icom_id)=4)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/81c8380d-4c95-40e6-887a-9d53658d52c2)


**Question 9**
---
![image](https://github.com/user-attachments/assets/25f85000-a317-4c56-87d7-2be074c68a59)


```sql
alter table Student_details add ParentsNumber number;
alter table Student_details add Adhar_Number number;
```

**Output:**

![image](https://github.com/user-attachments/assets/0dab410d-f53d-46fb-a632-a5d2446db961)


**Question 10**
---
![image](https://github.com/user-attachments/assets/54093773-2cb6-4eb7-84e8-ff6a44afcff3)


```sql
create table contacts(
contact_id INTEGER primary key,
first_name TEXT not NULL,
last_name TEXT not NULL,
email TEXT,
phone TEXT not NULL check(length(phone)=10)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/d114a18a-7678-4a0f-b16a-056925332f2e)



## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
