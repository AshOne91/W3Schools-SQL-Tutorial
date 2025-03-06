# SQL HAVING 절
## SQL HAVING 절
`HAVING` 절은 SQL에 추가되어졌다. 왜냐면 `WHERE`키워드는 집계함수와 같이 사용되어 질 수 없다.
## HAVING 문법
```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s)
```
## SQL HAVING 예제
다음 SQL 문은 각 국가의 고객 수를 나열합니다. 고객이 5명 이상인 국가만 포함합니다.
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5;
```
다음 SQL 문은 각 국가의 고객 수를 높은 순서에서 낮은 순서로 정렬하여 나열합니다(고객이 5명 이상인 국가만 포함).
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5
ORDER BY COUNT(CustomerID) DESC;
```
## More HAVING Examples
다음 SQL 문은 10개 이상의 주문을 등록한 직원을 나열합니다.
```sql
SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders
FROM (Orders
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID)
GROUP BY LastName
HAVING COUNT(Orders.OrderID) > 10;
```
다음 SQL 문은 직원 "Davolio" 또는 "Fuller"가 25개 이상의 주문을 등록했는지 여부를 나열합니다.
```sql
SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders
FROM Orders
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
WHERE LastName = 'Davolio' OR LastName = 'Fuller'
GROUP BY LastName
HAVING COUNT(Orders.OrderID) > 25;
```
