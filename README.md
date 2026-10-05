# 📊 SQL Assignment 1 — Sales Order Processing System

## 📌 Project Overview

This project is based on **ABC Fashion**, a retail organization with a Sales Order Processing System used to manage customers, sales representatives, and customer orders.

The assignment focuses on applying SQL concepts to retrieve and manipulate sales-related data across the **Salesman, Customer, and Orders** tables.

---

## 🏢 Business Scenario

**ABC Fashion** is a leading retailer with a large customer base and a team of sales representatives.

The Sales Order Processing System manages information related to:

- 👨‍💼 Sales representatives
- 👤 Customers
- 🛒 Customer orders
- 💰 Purchase amounts
- 📍 Salesman locations
- 💵 Sales commissions

---

## 🎯 Assignment Objectives

The assignment covers the following SQL tasks:

### 1. Insert a New Order

Insert a new record into the **Orders** table.

**Concepts used:**
- `INSERT INTO`
- Data insertion

---

### 2. Apply Table Constraints

Implement the required constraints:

**Salesman Table**
- Add a **Primary Key** constraint to `SalesmanId`
- Add a **Default** constraint to the `City` column

**Customer Table**
- Add a **Foreign Key** constraint to `SalesmanId`
- Add a **NOT NULL** constraint to `Customer_name`

**Concepts used:**

```text
PRIMARY KEY
FOREIGN KEY
DEFAULT
NOT NULL
ALTER TABLE
```

These requirements are specified in the assignment.

---

### 3. Filter Customer and Purchase Data

Retrieve records where:

- Customer name ends with **`N`**
- Purchase amount is **greater than 500**

Example:

```sql
SELECT *
FROM Orders
WHERE Customer_name LIKE '%N'
  AND Purchase_amount > 500;
```

The assignment specifically requires both conditions.

---

### 4. Use SQL SET Operators

Retrieve `SalesmanId` values from two tables.

#### UNION — Unique Values

```sql
SELECT SalesmanId
FROM Salesman

UNION

SELECT SalesmanId
FROM Orders;
```

#### UNION ALL — Including Duplicates

```sql
SELECT SalesmanId
FROM Salesman

UNION ALL

SELECT SalesmanId
FROM Orders;
```

This demonstrates the difference between `UNION` and `UNION ALL`.

---

### 5. Retrieve Matching Sales Information

Display:

- `Orderdate`
- `Salesman Name`
- `Customer Name`
- `Commission`
- `City`

for records where the **Purchase Amount is between 500 and 1500**.

Example filtering condition:

```sql
WHERE Purchase_amount BETWEEN 500 AND 1500;
```

This task involves retrieving matching information from the relevant tables.

---

### 6. Use RIGHT JOIN

Use a **RIGHT JOIN** between the `Salesman` and `Orders` tables to retrieve the required results.

Example:

```sql
SELECT *
FROM Salesman S
RIGHT JOIN Orders O
    ON S.SalesmanId = O.SalesmanId;
```

The assignment specifically requires a RIGHT JOIN between these two tables.

---

# 🧠 SQL Concepts Practiced

| SQL Concept | Purpose |
|---|---|
| `INSERT INTO` | Insert new records |
| `ALTER TABLE` | Modify table structure |
| `PRIMARY KEY` | Uniquely identify records |
| `FOREIGN KEY` | Establish relationships between tables |
| `DEFAULT` | Assign a default value |
| `NOT NULL` | Prevent NULL values |
| `WHERE` | Filter records |
| `LIKE` | Pattern matching |
| `AND` | Combine conditions |
| `BETWEEN` | Filter values within a range |
| `UNION` | Return unique values |
| `UNION ALL` | Return values including duplicates |
| `RIGHT JOIN` | Retrieve records using a right-side table |

---

# 📁 Repository Structure

```text
SQL-Assignment-1/
│
├── README.md
│
├── Dataset/
|     |__ Salesman.sql
|     |__ Customer.sql
|     |__ Orders.sql
│
└── SQL-Assignment-1_Task.sql/
    └── Task.sql
```


# 🛠️ Tools & Technologies

- **SQL**
- **SQL Server**
- **GitHub**

---

# 📚 Learning Outcomes

By completing this assignment, I practiced:

- Working with relational database tables
- Inserting records into tables
- Applying database constraints
- Filtering data using conditions
- Performing pattern matching with `LIKE`
- Using `UNION` and `UNION ALL`
- Joining data from multiple tables
- Using `BETWEEN` for range-based filtering
- Applying `RIGHT JOIN`
- Understanding relationships between database tables

---

# 📌 Assignment Tasks Summary

| # | Task | Main SQL Concept |
|---|---|---|
| 1 | Insert a new order | `INSERT INTO` |
| 2 | Add table constraints | `ALTER TABLE`, Constraints |
| 3 | Filter customers and purchase amount | `LIKE`, `WHERE` |
| 4 | Retrieve unique and duplicate Salesman IDs | `UNION`, `UNION ALL` |
| 5 | Display matching sales information | Joins, `BETWEEN` |
| 6 | Retrieve Salesman and Orders data | `RIGHT JOIN` |

The six tasks are taken directly from the assignment requirements.

---

## 👩‍💻 Author

**Pournami Manthodi**

🎓 MSc Mathematics  
📊 Data Analytics & Data Science  

**Skills:**  
`SQL` • `Python` • `Excel` • `Power BI` • `Tableau`

---

⭐ **This project demonstrates practical SQL skills through a retail sales order processing use case.**
