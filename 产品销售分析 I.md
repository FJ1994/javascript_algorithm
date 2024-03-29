> 题目

销售表 Sales：

+-------------+-------+
| Column Name | Type  |
+-------------+-------+
| sale_id     | int   |
| product_id  | int   |
| year        | int   |
| quantity    | int   |
| price       | int   |
+-------------+-------+
(sale_id, year) 是销售表 Sales 的主键.
product_id 是产品表 Product 的外键.
注意: price 表示每单位价格
产品表 Product：

+--------------+---------+
| Column Name  | Type    |
+--------------+---------+
| product_id   | int     |
| product_name | varchar |
+--------------+---------+
product_id 是表的主键.
写一条SQL 查询语句获取产品表 Product 中所有的 产品名称 product name 以及 该产品在 Sales 表中相对应的 上市年份 year 和 价格 price。

示例：

Sales 表：
+---------+------------+------+----------+-------+
| sale_id | product_id | year | quantity | price |
+---------+------------+------+----------+-------+ 
| 1       | 100        | 2008 | 10       | 5000  |
| 2       | 100        | 2009 | 12       | 5000  |
| 7       | 200        | 2011 | 15       | 9000  |
+---------+------------+------+----------+-------+

Product 表：
+------------+--------------+
| product_id | product_name |
+------------+--------------+
| 100        | Nokia        |
| 200        | Apple        |
| 300        | Samsung      |
+------------+--------------+

Result 表：
+--------------+-------+-------+
| product_name | year  | price |
+--------------+-------+-------+
| Nokia        | 2008  | 5000  |
| Nokia        | 2009  | 5000  |
| Apple        | 2011  | 9000  |
+--------------+-------+-------+

来源：力扣（LeetCode）
链接：https://leetcode-cn.com/problems/product-sales-analysis-i
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

> 解题思路（一）

* 一个`inner join`搞定

> 实现代码（一）

```sql
# Write your MySQL query statement below

SELECT P.PRODUCT_NAME, S.YEAR, S.PRICE FROM PRODUCT P INNER JOIN SALES S ON S.PRODUCT_ID = P.PRODUCT_ID
```

> 解题思路（二）

* `WHERE`条件判断

> 实现代码（二）

```sql
# Write your MySQL query statement below

SELECT P.PRODUCT_NAME, S.YEAR, S.PRICE FROM PRODUCT P, SALES S WHERE S.PRODUCT_ID = P.PRODUCT_ID
```