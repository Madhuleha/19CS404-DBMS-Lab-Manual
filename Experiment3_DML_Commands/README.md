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
<img width="712" height="229" alt="image" src="https://github.com/user-attachments/assets/1ef7d835-c8e6-4db5-a3ba-218a3d15a829" />

```sql
UPDATE products
SET availability  = availability  * 2
WHERE product_id = 1;
```

**Output:**

<img width="1189" height="183" alt="image" src="https://github.com/user-attachments/assets/1cc81747-1e9a-4d14-993a-e8b6bf32c03d" />



**Question 2**
---
<img width="1245" height="693" alt="image" src="https://github.com/user-attachments/assets/4d38a031-d452-43ba-87cb-9d009278fc33" />

```sql
UPDATE employees  
SET salary = CASE
    WHEN department_id = 40 THEN ROUND (salary * 1.25)
    WHEN department_id = 90 THEN ROUND (salary * 1.15)
    WHEN department_id = 110 THEN ROUND (salary * 1.10) 
    ELSE salary
END;
```

**Output:**

<img width="1204" height="215" alt="image" src="https://github.com/user-attachments/assets/c46b1757-fb79-41ce-907f-21bca0d69ca8" />


**Question 3**
---
<img width="1205" height="641" alt="image" src="https://github.com/user-attachments/assets/5cd27b63-affd-442f-8d58-0a0b04c745c2" />

```sql
UPDATE EMPLOYEES
SET EMAIL = 'not available',
    COMMISSION_PCT = 0.55
WHERE DEPARTMENT_ID = 110;
```
**Output:**

<img width="1269" height="284" alt="image" src="https://github.com/user-attachments/assets/9bebe57c-f4a8-47ee-9aa5-afd48c82a4f1" />


**Question 4**
---
<img width="880" height="314" alt="image" src="https://github.com/user-attachments/assets/714eb1a7-d31a-4d4f-8431-492af116cc6f" />

```sql
UPDATE PRODUCTS
SET QUANTITY = QUANTITY * 1.10;
```
**Output:**

<img width="1092" height="296" alt="image" src="https://github.com/user-attachments/assets/c9740a98-4ec1-4cec-84c7-42ba40d1d695" />

**Question 5**
---
<img width="1201" height="636" alt="image" src="https://github.com/user-attachments/assets/dce457fd-4b63-42b6-8f9a-ef207b8e92e4" />

```sql
UPDATE purchases
SET per_unit_price = 25,
    total_price = quantity * 25
WHERE purchase_date = '2022-08-15'
    AND product_id = 12;
```

**Output:**

<img width="1303" height="252" alt="image" src="https://github.com/user-attachments/assets/74cb87ff-ddb1-4de1-985a-9f3167dc7485" />

**Question 6**
---
<img width="1271" height="366" alt="image" src="https://github.com/user-attachments/assets/38f05b35-fd2b-4e21-b5a2-5279faa4bf6b" />

```sql
DELETE FROM Customer
WHERE (GRADE = 3 OR AGENT_CODE = 'A008')
    AND OUTSTANDING_AMT < 5000;
```

**Output:**

<img width="1080" height="128" alt="image" src="https://github.com/user-attachments/assets/26b7e75e-9a12-42d7-a1f3-8c653a76446b" />

**Question 7**
---
<img width="1274" height="377" alt="image" src="https://github.com/user-attachments/assets/ac6bdea9-582f-485f-9d9f-076a12701cf5" />

```sql
DELETE FROM customer
WHERE GRADE % 2 = 1;
```

**Output:**

<img width="1089" height="136" alt="image" src="https://github.com/user-attachments/assets/e6d4b247-201d-4ea9-8562-29a7a226b611" />

**Question 8**
---
<img width="1283" height="460" alt="image" src="https://github.com/user-attachments/assets/c512ce6c-168c-472b-90db-8ada1fa35236" />

```sql
DELETE FROM customer
WHERE cust_name LIKE '%Holmes%';
```

**Output:**

<img width="1104" height="175" alt="image" src="https://github.com/user-attachments/assets/1fcc47f3-4b1e-4856-973d-cfbdda77f658" />

**Question 9**
---
<img width="1277" height="378" alt="image" src="https://github.com/user-attachments/assets/991849c3-98dc-423a-8ee3-89370c5cd9dc" />

```sql
DELETE FROM customer
WHERE CUST_CITY <> 'New York'
    AND OUTSTANDING_AMT > 5000;
```

**Output:**

<img width="1112" height="194" alt="image" src="https://github.com/user-attachments/assets/d1d31407-5af8-4766-bffb-8533f407d92b" />


**Question 10**
---
<img width="1277" height="561" alt="image" src="https://github.com/user-attachments/assets/47d94311-ae9a-467f-8697-fc7618b92327" />

```sql
DELETE FROM customer
WHERE GRADE = 2;
```

**Output:**

<img width="723" height="568" alt="image" src="https://github.com/user-attachments/assets/295ce263-307c-4e20-b5a3-3655d23abc7b" />
<img width="1867" height="921" alt="image" src="https://github.com/user-attachments/assets/f4030864-544a-4257-8cc4-fe42874fa144" />

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
