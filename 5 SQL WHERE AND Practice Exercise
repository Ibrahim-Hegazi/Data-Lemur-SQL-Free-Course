# SQL Practice - Multi-Condition Review Filtering
This repository contains a SQL solution for filtering Amazon reviews using multiple WHERE conditions with AND.

## 📌 Problem Link
[SQL WHERE AND Practice Exercise - DataLemur](https://datalemur.com/questions/sql-where-and-practice-exercise)

## 🧠 Problem Description
Filter Amazon reviews based on 4 conditions:
1. Review has 4 or more stars
2. Review ID is less than 6000
3. Review ID is more than 2000
4. Review cannot come from user 142

## 🧾 Table Schema
### reviews

| Column Name   | Type      | Description                  |
|---------------|-----------|------------------------------|
| review_id     | integer   | Unique ID of the review      |
| user_id       | integer   | ID of the user who reviewed  |
| submit_date   | datetime  | Date when review was submitted|
| product_id    | integer   | ID of the reviewed product   |
| stars         | integer   | Star rating (1-5)            |

## 🧪 Example Input
| review_id | user_id | submit_date           | product_id | stars |
|-----------|---------|-----------------------|------------|-------|
| 6171      | 123     | 06/08/2022 00:00:00   | 50001      | 4     |
| 4582      | 562     | 06/15/2022 00:00:00   | 12580      | 4     |
| 7802      | 265     | 06/10/2022 00:00:00   | 69852      | 4     |
| 5293      | 362     | 06/18/2022 00:00:00   | 50001      | 3     |
| 6352      | 192     | 07/26/2022 00:00:00   | 69852      | 3     |
| 4517      | 981     | 07/05/2022 00:00:00   | 69852      | 2     |

## ✅ Expected Output
| review_id | user_id | submit_date           | product_id | stars |
|-----------|---------|-----------------------|------------|-------|
| 4582      | 562     | 06/15/2022 00:00:00   | 12580      | 4     |

## 💡 Correct SQL Solution
```sql
SELECT * 
FROM reviews
WHERE stars >= 4 
  AND review_id < 6000 
  AND review_id > 2000 
  AND user_id != 142;
