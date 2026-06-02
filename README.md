# 🏥 Hospital Management SQL – Task 3

## 📌 Elevate Labs SQL Developer Internship – Task 3

This project was completed as part of the **Elevate Labs SQL Developer Internship – Task 3: Writing Basic SELECT Queries**.

This task focused on learning how to retrieve and filter data using SQL queries. The database schema created in **Task 1 (Schema Design)** and data manipulation performed in **Task 2 (DML Operations)** were reused to continue working on a Hospital Management Database System.

The task emphasized learning:

- `SELECT`
- `WHERE`
- `AND`
- `OR`
- `LIKE`
- `BETWEEN`
- `ORDER BY`
- `LIMIT`

for retrieving and filtering records from database tables.

---

# 🎯 Objective

The objective of this task was to:

- Retrieve data from one or more tables
- Learn filtering using conditions
- Sort records
- Limit query output
- Practice projection (specific column selection)
- Understand SQL retrieval operations

---

# 🏥 Project Overview

This project continues the **Hospital Management Database System** created during previous internship tasks.

The following tables were reused:

- Patients
- Doctors
- Departments
- Appointments

The database was queried using SQL to retrieve specific information and filter records based on different conditions.

---

# 🛠 Tools Used

- PostgreSQL
- pgAdmin 4
- SQL (SELECT Queries)
- GitHub

---

# 🗂 Existing Database Schema Used

## 1. Patients Table

Stores patient information.

Columns:
- patient_id
- patient_name
- age
- gender
- phone_number

---

## 2. Doctors Table

Stores doctor information.

Columns:
- doctor_id
- doctor_name
- specialization
- phone_number

---

## 3. Departments Table

Stores department information.

Columns:
- department_id
- department_name

---

## 4. Appointments Table

Stores appointment details.

Columns:
- appointment_id
- patient_id
- doctor_id
- department_id
- appointment_date

---

# ⚙️ Step-by-Step Process Followed

## Step 1: Retrieve All Records

Used:

```sql
SELECT * FROM patients;
```

### What was learned

- `SELECT *` retrieves all rows and columns
- Useful for viewing complete table data

---

## Step 2: Retrieve Specific Columns (Projection)

Used:

```sql
SELECT patient_name, age
FROM patients;
```

### What was learned

- Specific columns can be selected
- Improves readability
- Avoids retrieving unnecessary data

---

## Step 3: Filtering Using WHERE

Used:

```sql
SELECT *
FROM patients
WHERE age > 25;
```

### What was learned

- `WHERE` filters rows
- Only matching records are returned

---

## Step 4: Filtering Using AND

Used:

```sql
SELECT *
FROM patients
WHERE age > 25
AND gender = 'Female';
```

### What was learned

- `AND` requires all conditions to be true

---

## Step 5: Filtering Using OR

Used:

```sql
SELECT *
FROM patients
WHERE patient_name = 'Priya'
OR patient_name = 'Rahul';
```

### What was learned

- `OR` returns rows if any condition is true

---

## Step 6: Pattern Matching Using LIKE

Used:

```sql
SELECT *
FROM patients
WHERE patient_name LIKE 'A%';
```

```sql
SELECT *
FROM patients
WHERE patient_name LIKE '%a';
```

```sql
SELECT *
FROM patients
WHERE patient_name LIKE '%av%';
```

### What was learned

- `LIKE` is used for pattern matching
- `A%` → starts with A
- `%a` → ends with a
- `%value%` → contains value

---

## Step 7: Filtering Using BETWEEN

Used:

```sql
SELECT *
FROM patients
WHERE age BETWEEN 25 AND 35;
```

### What was learned

- `BETWEEN` filters values within a range
- Includes both start and end values

---

## Step 8: Sorting Using ORDER BY

Used:

```sql
SELECT *
FROM patients
ORDER BY age;
```

and

```sql
SELECT *
FROM patients
ORDER BY age DESC;
```

### What was learned

- Default sorting is ascending (`ASC`)
- `DESC` sorts values in descending order

---

## Step 9: Limiting Output Rows

Used:

```sql
SELECT *
FROM patients
LIMIT 3;
```

```sql
SELECT *
FROM patients
ORDER BY age DESC
LIMIT 2;
```

### What was learned

- `LIMIT` restricts number of rows returned
- Useful for previews and top results

---

## Step 10: Removing Duplicates Using DISTINCT

Used:

```sql
SELECT DISTINCT gender
FROM patients;
```

### What was learned

- `DISTINCT` removes duplicate values

---

## Step 11: Aliasing Columns

Used:

```sql
SELECT patient_name AS Name,
age AS Patient_Age
FROM patients;
```

### What was learned

- `AS` renames columns temporarily
- Improves readability

---

# 🧠 Key Concepts Learned

- SELECT Statement
- Projection
- Filtering
- WHERE Clause
- AND Operator
- OR Operator
- LIKE Operator
- BETWEEN Operator
- ORDER BY
- LIMIT
- DISTINCT
- Aliasing

---

# ❓ Interview Questions and Answers

## 1. What does SELECT * do?

It retrieves all rows and columns from a table.

---

## 2. How do you filter rows?

Using:

```sql
WHERE
```

clause.

---

## 3. What is LIKE '%value%'?

It searches for rows containing a specific pattern.

Example:

```sql
LIKE '%av%'
```

returns values containing `av`.

---

## 4. What is BETWEEN used for?

Used for filtering values within a range.

---

## 5. How do you limit output rows?

Using:

```sql
LIMIT
```

---

## 6. Difference between = and IN

`=` compares one value.

Example:

```sql
WHERE age = 25
```

`IN` compares multiple values.

Example:

```sql
WHERE age IN (25,30,35)
```

---

## 7. How to sort in descending order?

Using:

```sql
ORDER BY column_name DESC
```

---

## 8. What is aliasing?

Temporarily renaming columns or tables using:

```sql
AS
```

---

## 9. Explain DISTINCT

`DISTINCT` removes duplicate values.

---

## 10. What is the default sort order?

Ascending (`ASC`)

---

# 🚧 Challenges Faced and Solutions

## 1. Database Connection Issue

### Problem

Received:

```text
relation "patients" does not exist
```

### Reason

Query tool was connected to the default `postgres` database instead of:

```text
hospital_management
```

### Solution

Switched to the correct database and executed queries again.

---

## 2. PostgreSQL Table Naming Confusion

### Problem

Confusion regarding:

```sql
Patients
```

vs

```sql
patients
```

### Reason

PostgreSQL converts table names to lowercase by default.

### Solution

Used lowercase table names consistently.

---

## 3. Understanding Filtering Conditions

### Problem

Confusion between:

- `AND`
- `OR`
- `LIKE`
- `BETWEEN`

### Solution

Practiced multiple queries to understand filtering behavior.

---

# 📂 Project Structure

```text
hospital-management-select-queries/
│── task3_select_queries.sql
│── README.md
```

---

# ✅ Outcome

Successfully practiced SQL retrieval operations by writing multiple SELECT queries to retrieve, filter, sort, and limit records in a Hospital Management Database System.

This task improved understanding of:

- Data retrieval
- Filtering
- Sorting
- Projection
- Query optimization basics
- SQL querying concepts

---

## 👩‍💻 Author

**Yaswinipriya Sesetti**

LinkedIn:  
https://www.linkedin.com/in/sesetti-yaswini-priya-95811925a
