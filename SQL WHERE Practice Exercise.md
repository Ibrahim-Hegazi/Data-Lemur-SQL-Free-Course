# ⭐ SQL Practice – 3-Star Reviews

This repository contains a simple SQL solution to a filtering problem using the `WHERE` clause.

---

## 📌 Problem Link

[3-Star Reviews – DataLemur SQL Practice](https://datalemur.com/questions/sql-where-practice-exercise)

---

## 🧠 Problem Description

You're given a table called `reviews` with the following columns:

- `user_id`: ID of the user who left the review  
- `stars`: The star rating left by the user (typically 1–5)

**Task:**  
Write a SQL query to return the `user_id` and `stars` **only for reviews that have exactly 3 stars**.

---

## ✅ Solution

```sql
SELECT user_id, stars
FROM reviews
WHERE stars = 3;
