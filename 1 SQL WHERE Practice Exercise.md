# ⭐ SQL Practice – 3-Star Reviews

This repository contains a simple SQL solution to a filtering problem using the `WHERE` clause.

---

## 📌 Problem Link

[3-Star Reviews – DataLemur SQL Practice](https://datalemur.com/questions/sql-where-practice-exercise)

---

## 🧠 Problem Description

You're given a table called `reviews` with the following columns:

- `review_id`: Unique ID of the review
- `user_id`: ID of the user who left the review  
- `submit_date`: Date the review was submitted
- `product_id`: ID of the product being reviewed
- `stars`: The star rating left by the user (1–5)

**Task:**  
Write a SQL query to return the `user_id` and `stars` **only for reviews that have exactly 3 stars**.

---

## 🧾 Table Schema

**reviews**

| Column Name | Type         |
|-------------|--------------|
| review_id   | integer      |
| user_id     | integer      |
| submit_date | datetime     |
| product_id  | integer      |
| stars       | integer (1–5)|

---

## 🧪 Example Input

| review_id | user_id | submit_date         | product_id | stars |
|-----------|---------|---------------------|------------|-------|
| 6171      | 123     | 06/08/2022 00:00:00 | 50001      | 4     |
| 7802      | 265     | 06/10/2022 00:00:00 | 69852      | 4     |
| 5293      | 362     | 06/18/2022 00:00:00 | 50001      | 3     |
| 6352      | 192     | 07/26/2022 00:00:00 | 69852      | 3     |
| 4517      | 981     | 07/05/2022 00:00:00 | 69852      | 2     |

---

## ✅ Expected Output

| user_id | stars |
|---------|-------|
| 362     | 3     |
| 192     | 3     |

---

## 💡 SQL Solution

```sql
SELECT user_id, stars
FROM reviews
WHERE stars = 3;
