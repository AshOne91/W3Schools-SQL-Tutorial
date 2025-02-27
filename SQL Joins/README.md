# SQL Joins
## SQL JOIN
`JOIN`절은 열의 조합에 사용되어진다 두개 혹은 그 이상의 테이블로 부터, 그들 사이의 관계된 컬럼을 기반으로
```sql
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders INNER JOIN Customers
ON Orders.CustomerID = CUstomers.CustomerID;
```
