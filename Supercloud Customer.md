# ☁️ SQL Challenge – Supercloud Customers

This repository contains the SQL solution to identify "Supercloud" customers — those who have purchased **at least one product from every product category**.

---

## 📌 Problem Link

[Supercloud Customers – DataLemur SQL Practice](https://datalemur.com/questions/supercloud-customer)

---

## 🧠 Problem Description

A **Microsoft Azure Supercloud customer** is defined as a customer who has purchased **at least one product from every product category** listed in the `products` table.

### ✅ Task:

Write a SQL query to return the **customer IDs** of these Supercloud customers.

---

## 🧾 Table Schemas

### `customer_contracts`

| Column Name  | Type    |
|--------------|---------|
| customer_id  | integer |
| product_id   | integer |
| amount       | integer |

### `products`

| Column Name       | Type    |
|-------------------|---------|
| product_id        | integer |
| product_category  | string  |
| product_name      | string  |

---

## 🧪 Example Input

### customer_contracts

| customer_id | product_id | amount |
|-------------|------------|--------|
| 1           | 1          | 1000   |
| 1           | 3          | 2000   |
| 1           | 5          | 1500   |
| 2           | 2          | 3000   |
| 2           | 6          | 2000   |

### products

| product_id | product_category | product_name             |
|------------|------------------|--------------------------|
| 1          | Analytics        | Azure Databricks         |
| 2          | Analytics        | Azure Stream Analytics   |
| 4          | Containers       | Azure Kubernetes Service |
| 5          | Containers       | Azure Service Fabric     |
| 6          | Compute          | Virtual Machines         |
| 7          | Compute          | Azure Functions          |

---

## ✅ Expected Output

| customer_id |
|-------------|
| 1           |

**Explanation:**  
Customer 1 bought from all 3 categories: **Analytics**, **Containers**, and **Compute**.  
Customer 2 did **not** purchase any container-related products.

---

## 💡 SQL Solution

```sql
WITH total_categories AS (
  SELECT COUNT(DISTINCT product_category) AS total_cat_count
  FROM products
),

customer_categories AS (
  SELECT 
    customer_id, 
    COUNT(DISTINCT product_category) AS cat_count
  FROM customer_contracts AS cc
  LEFT JOIN products AS p 
    ON cc.product_id = p.product_id
  GROUP BY customer_id
)

SELECT customer_id
FROM customer_categories 
CROSS JOIN total_categories
WHERE cat_count = total_cat_count;
