# SQL Joins
## SQL JOIN
`JOIN`절은 열의 조합에 사용되어진다 두개 혹은 그 이상의 테이블로 부터, 그들 사이의 관계된 컬럼을 기반으로
```sql
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders INNER JOIN Customers
ON Orders.CustomerID = CUstomers.CustomerID;
```
## Different Types of SQL JOINs
SQL에서 조인들의 타입에 따른 다른점
-(INNER) JOIN : 양쪽 테이블에 매칭되는 값을 가지는 레코드를 반환한다.
-LEFT (OUTER) JOIN : 왼쪽 테이블에 모든 레코드를 반환한다, 그리고 매치된 오른쪽 테이블에서 레코드
-RIGHT (OUTER) JOIN : 오른쪽 테이블에 모든 레코드를 반환한다, 그리고 매치된 왼쪽 테이블의 레코드도
-FULL (OUTER) JOIN : 매치된 왼쪽 또는 오른쪽 테이블의 모든 레코드를 반환한다



