
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
[1378. Replace Employee ID With The Unique Identifier](https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/)
```sql
SELECT EmployeeUNI.unique_id,Employees.name
FROM employees
Natural Left Join EmployeeUNI;
```
[1068. Product Sales Analysis I](https://leetcode.com/problems/product-sales-analysis-i/)
```sql
SELECT product_name , year , price 
FROM sales
JOIN product ON sales.product_id  = product.product_id;
```
[1581. Customer Who Visited but Did Not Make Any Transactions](https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/)
```sql
SELECT customer_id , count(visit_id) as count_no_trans
FROM Visits
WHERE visit_id not in (SELECT visit_id FROM Transactions )
GROUP BY customer_id;
```
[197. Rising Temperature](https://leetcode.com/problems/rising-temperature/)
```sql
Select a.id
From Weather a Join Weather b
On a.recordDate  = DATEADD(day,1,b.recordDate )
Where a.temperature > b.temperature; 
```
[1661. Average Time of Process per Machine](https://leetcode.com/problems/average-time-of-process-per-machine/)
```sql

Select a.machine_id, round ( Avg(b.timestamp- a.timestamp),3)as processing_time
From Activity a
Join Activity b
On a.machine_id= b.machine_id
And a.process_id = b.process_id
And a.activity_type ='start' And b.activity_type = 'end'
Group by a.machine_id;

```
[577. Employee Bonus](leetcode.com/problems/employee-bonus/)
```sql
Select name, bonus
From Employee e Left join Bonus b
On e.empId = b.empId
Where bonus < 1000 Or bonus IS NULL;

```

