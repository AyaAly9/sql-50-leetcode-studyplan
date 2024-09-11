
# SQL 50 - LeetCode
Solutions for [SQL 50 Study Plan](https://leetcode.com/studyplan/top-sql-50/) on LeetCode

---
[1757 - Recyclable and Low Fat Products](https://leetcode.com/problems/recyclable-and-low-fat-products/)
```sql

SELECT product_id
FROM products
WHERE low_fats='Y' AND recyclable='Y';
```

[584 -Find Customer Referee](https://leetcode.com/problems/find-customer-referee/)
```sql

SELECT name
FROM Customer
WHERE referee_id !=2 OR referee_id IS null;
```
[595. Big Countries](https://leetcode.com/problems/big-countries/)
```sql
SELECT name,population ,area
FROM World
WHERE area >= 3000000 OR population >=25000000;
```
[1148. Article Views I](https://leetcode.com/problems/article-views-i/)
```sql
SELECT DISTINCT author_id as id
FROM Views
WHERE viewer_id = author_id
ORDER by id ;
```
[1683. Invalid Tweets](https://leetcode.com/problems/invalid-tweets/)
```sql
SELECT tweet_id
FROM Tweets
WHERE LENGTH(content) > 15;
```
