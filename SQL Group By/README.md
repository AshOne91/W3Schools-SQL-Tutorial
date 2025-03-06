# SQL GROUP BY Statement
## The SQL GROUP BY Statement
`GROUP BY` 문장은 그룹한다. 행을 같은 값을 가지는 행들의 요약으로, 마치 "각 국가의 고객 수를 찾아보세요."
`GROUP BY` 문장은 종종 사용되어진다. 집계함수들과 (`COUNT()`, `MAX()`, `MIN()`, `SUM()`, `AVG()`) 하나 이상의 열로 그룹화하기 위해
## GROUP BY Syntax
```python
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s)
```
## SQL GROUP BY Examples
The following SQL statement lists the number of customers in each country:
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country;
```
The following SQL statement lists the number of customers in each country, sorted high to low:
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
ORDER BY COUNT(CustomerID) DESC;
```
## GROUP BY With JOIN Example
The following SQL statement lists the number of orders sent by each shipper:
```sql
SELECT Shippers.ShipperName, COUNT(Orders.OrderID) AS NumberOfOrders FROM
Orders
LEFT JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID
GROUP BY ShipperName;
```
