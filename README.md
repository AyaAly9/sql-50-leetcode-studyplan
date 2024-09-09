
# SQL 50 - LeetCode
Solutions for [SQL 50 Study Plan](https://leetcode.com/studyplan/top-sql-50/) on LeetCode
[1757 - Recyclable and Low Fat Products](https://leetcode.com/problems/recyclable-and-low-fat-products/)
```sql
SELECT product_id
FROM products
WHERE low_fats='Y' AND recyclable='Y';

[584 - Find Customer Referee](https://leetcode.com/problems/find-customer-referee)
```sql
SELECT name
FROM Customer
WHERE referee_id !=2 OR referee_id IS null;
