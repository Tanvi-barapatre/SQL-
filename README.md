# 🗄️ SQL — From Zero to Advanced

**Learning SQL one query at a time — from understanding databases to writing advanced queries and solving real-world data problems.**

![SQL](https://img.shields.io/badge/SQL-Learning-blue?style=for-the-badge)
![Database](https://img.shields.io/badge/Database-MySQL-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=for-the-badge)

---

## 🚀 About This Repository

This repository documents my **SQL learning journey**, starting from the fundamentals and gradually progressing toward advanced SQL concepts.

I'm not just focusing on memorizing SQL syntax. My goal is to understand:

- 🧠 **How databases work**
- 🔎 **How to retrieve and analyze data**
- 🏗️ **How database structures are created**
- ✏️ **How data is inserted, updated and deleted**
- 🔗 **How multiple tables are connected**
- 📊 **How SQL can be used for data analysis**
- ⚡ **How SQL queries can be optimized**
- 🏢 **How SQL is used in real-world data projects**

This repository contains my **notes, queries, practice exercises, examples and projects** as I learn.

---

## 🎯 Learning Goal

The goal is to go from:

```text
SQL Beginner
     ↓
Basic Queries
     ↓
Database & Table Operations
     ↓
Filtering & Data Manipulation
     ↓
Joins & Functions
     ↓
Aggregations & Window Functions
     ↓
Advanced SQL
     ↓
Query Optimization
     ↓
Real-World Projects
```

Ultimately, I want to be able to look at a data problem and think:

> **"I know how to get the answer using SQL."** 💡

---

# 📚 What I'm Learning

## 🟢 Beginner Level

### 1. Introduction to SQL
- What is SQL?
- Why SQL?
- What is a Database?
- Types of Databases
- SQL vs Database
- SQL Commands
- SQL in Data Analytics & Data Engineering

### 2. Environment Setup
- SQL Server / Database setup
- MySQL / SQL tools
- Database and dataset preparation
- Working with SQL environments

### 3. Querying Data
Learning how to retrieve information from databases using:

```sql
SELECT
FROM
WHERE
```

Understanding how a SQL query asks a database a question and returns the required data.

### 4. DDL — Data Definition Language

Learning how to define and modify database structures:

```sql
CREATE
ALTER
DROP
```

### 5. DML — Data Manipulation Language

Learning how to work with the actual data stored inside tables:

```sql
INSERT
UPDATE
DELETE
```

---

# 🟡 Intermediate SQL

## 🔎 Filtering Data

Learning how to retrieve only the data that satisfies specific conditions.

Topics include:

- Comparison Operators
- Logical Operators
- `BETWEEN`
- `IN`
- `LIKE`
- Filtering with `WHERE`

Example:

```sql
SELECT *
FROM employees
WHERE salary > 50000;
```

---

## 🔗 SQL Joins

One of the most important SQL concepts.

Learning how to combine information from multiple tables.

Topics:

- `INNER JOIN`
- `LEFT JOIN`
- `RIGHT JOIN`
- `FULL OUTER JOIN`
- Advanced Joins
- Choosing the appropriate Join

Example:

```sql
SELECT
    customers.name,
    orders.order_date
FROM customers
INNER JOIN orders
    ON customers.customer_id = orders.customer_id;
```

---

## 🧩 Set Operators

Learning how to combine results from multiple queries:

```sql
UNION
UNION ALL
EXCEPT
INTERSECT
```

---

# 🛠️ SQL Functions

Learning how SQL can transform and analyze data.

### 🔤 String Functions

Working with text data.

### 🔢 Numeric Functions

Performing calculations and transformations.

### 📅 Date & Time Functions

Working with dates and timestamps.

### NULL Functions

Understanding and handling missing values.

### CASE Statements

Adding conditional logic to SQL queries.

Example:

```sql
CASE
    WHEN salary >= 100000 THEN 'High'
    WHEN salary >= 50000 THEN 'Medium'
    ELSE 'Low'
END
```

---

# 📊 Aggregate Functions

Learning how to summarize large amounts of data.

```sql
COUNT()
SUM()
AVG()
MIN()
MAX()
```

Combined with:

```sql
GROUP BY
HAVING
```

Example:

```sql
SELECT
    department,
    AVG(salary) AS average_salary
FROM employees
GROUP BY department;
```

---

# 🪟 Window Functions

Moving beyond traditional aggregation.

Topics include:

- Window Function Basics
- Window Aggregations
- Ranking Functions
- Value Functions

Important functions:

```sql
ROW_NUMBER()
RANK()
DENSE_RANK()
LAG()
LEAD()
FIRST_VALUE()
LAST_VALUE()
```

Example:

```sql
SELECT
    employee_name,
    salary,
    RANK() OVER (
        ORDER BY salary DESC
    ) AS salary_rank
FROM employees;
```

---

# 🔴 Advanced SQL

Taking SQL from query writing to professional-level usage.

### Topics

- Subqueries
- Common Table Expressions (CTEs)
- Views
- Temporary Tables
- CTAS
- Stored Procedures
- Triggers
- Indexes
- Execution Plans
- Table Partitioning
- Query Performance
- SQL + AI

---

# ⚡ SQL Performance

Learning that writing a query that **works** is not always enough.

A good SQL developer should also understand:

> **How efficiently does the database execute this query?**

Topics include:

- Execution Plans
- Indexes
- Partitioning
- Query Optimization
- Performance Tuning
- SQL Best Practices

---

# 🏢 Real-World SQL Projects

The final goal is to apply SQL to realistic problems rather than only practicing isolated queries.

### 🏗️ Project 1 — SQL Data Warehouse

Building a data warehouse using different layers:

```text
        Raw Data
           ↓
       🥉 Bronze
           ↓
       🥈 Silver
           ↓
        🥇 Gold
           ↓
      Business Data
```

### 📊 Project 2 — Exploratory Data Analysis

Using SQL to explore datasets and discover:

- Patterns
- Trends
- Relationships
- Business insights
- Interesting observations

### 📈 Project 3 — Advanced Data Analytics

Applying advanced SQL techniques to solve analytical problems and extract meaningful insights from data.

---

# 📂 Repository Structure

```text
SQL/
│
├── 01_Introduction/
│   ├── What_is_SQL
│   ├── Why_SQL
│   ├── Databases
│   └── SQL_Commands
│
├── 02_Basics/
│   ├── SELECT
│   ├── FROM
│   ├── WHERE
│   ├── DDL
│   └── DML
│
├── 03_Filtering/
│   ├── Operators
│   ├── BETWEEN
│   ├── IN
│   └── LIKE
│
├── 04_Joins/
│   ├── INNER_JOIN
│   ├── LEFT_JOIN
│   ├── RIGHT_JOIN
│   ├── FULL_JOIN
│   └── Advanced_Joins
│
├── 05_Functions/
│   ├── String
│   ├── Numeric
│   ├── Date_Time
│   └── NULL
│
├── 06_Aggregation/
│   ├── GROUP_BY
│   ├── HAVING
│   └── Aggregate_Functions
│
├── 07_Window_Functions/
│   ├── Ranking
│   ├── Aggregate
│   └── Value_Functions
│
├── 08_Advanced_SQL/
│   ├── Subqueries
│   ├── CTE
│   ├── Views
│   ├── Stored_Procedures
│   ├── Triggers
│   └── Indexes
│
├── 09_Performance/
│   ├── Execution_Plans
│   ├── Partitioning
│   └── Optimization
│
└── 10_Projects/
    ├── Data_Warehouse
    ├── EDA
    └── Advanced_Analytics
```

---

# 🧠 My Learning Philosophy

I'm following a simple rule:

```text
Learn → Understand → Write → Practice → Break → Debug → Repeat
```

I don't want this repository to be a collection of copied SQL queries.

I want it to represent **what I actually understand and can build with SQL.**

---

# 📌 Progress Tracker

| Topic | Status |
|---|:---:|
| Introduction to SQL | ⬜ |
| Database Fundamentals | ⬜ |
| SELECT Queries | ⬜ |
| DDL | ⬜ |
| DML | ⬜ |
| Filtering | ⬜ |
| Joins | ⬜ |
| Set Operators | ⬜ |
| SQL Functions | ⬜ |
| Aggregate Functions | ⬜ |
| GROUP BY / HAVING | ⬜ |
| Window Functions | ⬜ |
| Subqueries | ⬜ |
| CTEs | ⬜ |
| Views | ⬜ |
| Temporary Tables | ⬜ |
| Stored Procedures | ⬜ |
| Triggers | ⬜ |
| Indexes | ⬜ |
| Execution Plans | ⬜ |
| Partitioning | ⬜ |
| Performance Optimization | ⬜ |
| SQL Projects | ⬜ |

---

# 🎓 Learning Resource

I'm primarily following the **SQL Full Course for Beginners — From Zero to Hero** by **Data with Baraa**.

🎥 **Course:**  
https://youtu.be/SSKVgrwhzus

The course covers SQL from beginner fundamentals through advanced techniques and real-world projects.

---

# 🔥 Why SQL?

Because data is everywhere.

Companies collect enormous amounts of information, but raw data is not enough.

**SQL turns data into answers.**

```text
DATA
  ↓
SQL
  ↓
INFORMATION
  ↓
INSIGHTS
  ↓
DECISIONS
```

And that's exactly what I'm learning to do.

---

## 🚧 Status

**Currently Learning SQL**

This repository will continuously evolve as I learn new concepts, solve problems, and build projects.

> 💻 **One query at a time. One concept at a time. One step closer to becoming a better developer.**

---

### ⭐ If you're learning SQL too...

Feel free to explore the repository, compare approaches, practice the queries, and learn along with me.

**Let's turn data into answers. 🚀**
