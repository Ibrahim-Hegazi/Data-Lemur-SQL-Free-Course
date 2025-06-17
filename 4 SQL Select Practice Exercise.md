# SQL Practice - Select All Products
This repository contains a simple SQL solution to select all data from a products table.

## 📌 Problem Link
[SQL Select Practice Exercise - DataLemur](https://datalemur.com/questions/sql-select-practice-exercise)

## 🧠 Problem Description
You're given a table called `products` with information about Microsoft Azure cloud products. 

**Task:**  
Write a SQL query to return all columns and all rows from the products table.

## 🧾 Table Schema
### products

| Column Name        | Type    | Description                     |
|--------------------|---------|---------------------------------|
| product_id         | integer | Unique identifier for the product|
| product_category   | string  | Category of the product         |
| product_name       | string  | Name of the Azure product       |

## 🧪 Example Input
| product_id | product_category | product_name             |
|------------|------------------|--------------------------|
| 1          | Analytics        | Azure Databricks         |
| 2          | Analytics        | Azure Stream Analytics   |
| 3          | Containers       | Azure Kubernetes Service |
| 4          | Containers       | Azure Kubernetes Service |
| 5          | Containers       | Azure Service Fabric     |
| 6          | Compute          | Virtual Machines         |
| 7          | Compute          | Azure Functions          |

## ✅ Expected Output
The query should return the entire table exactly as shown in the example input.

## 💡 SQL Solution
```sql
SELECT * FROM products;
