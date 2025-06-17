# SQL Select Practice Exercise

## Problem Description
This is a basic SQL exercise focused on selecting all data from a table. Given a `products` table containing information about Microsoft Azure cloud products, write a query to output all columns and rows from the table.

## Table Structure
### products Table
| Column Name        | Type    | Description                     |
|--------------------|---------|---------------------------------|
| product_id         | integer | Unique identifier for the product|
| product_category   | string  | Category of the product         |
| product_name       | string  | Name of the Azure product       |

## Example Input
| product_id | product_category | product_name             |
|------------|------------------|--------------------------|
| 1          | Analytics        | Azure Databricks         |
| 2          | Analytics        | Azure Stream Analytics   |
| 3          | Containers       | Azure Kubernetes Service |
| 4          | Containers       | Azure Kubernetes Service |
| 5          | Containers       | Azure Service Fabric     |
| 6          | Compute          | Virtual Machines         |
| 7          | Compute          | Azure Functions          |

## Expected Output
The query should return all columns and all rows from the products table exactly as they appear in the database.

## Solution
```sql
SELECT * FROM products;
