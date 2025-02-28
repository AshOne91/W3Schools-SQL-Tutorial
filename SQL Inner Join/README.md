# SQL INNER JOIN
## INNER JOIN
`INNER JOIN` 키워드는 양 테이블에 매칭되는 값의 레코드들을 선택한다.
프러덕트 테이블과 합칠거다 카테고리 테이블이랑, 카테고리 아이디 필드를 사용해서 양쪽 테이블로 부터
```sql
SELECT ProductID, ProductName, CategoryName FROM Products INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID;
```
`INNER JOIN` 키워드는 오직 양쪽 테이플에서 매치된 열만 리턴한다. 만약 카테고리아이디가 없는 프러덕트는 카테고리 테이블에 표시할 수 없다.
## 문법
```sql
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name 
```
## 컬럼들의 네이밍
좋은 시도이다 테이블 이름을 포함하는거 컬럼을 지정하기위해 SQL 문장에서
```sql
SELECT Products.ProductID, Products.ProductName, Categories.CategoryName
FROM Products
INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID;
```
## JOIN or INNER JOIN
`JOIN` 그리고 `INNER JOIN` 같은 결과를 리턴한다
`INNER`는 `JOIN`으로 기본 조인 타입이다, 그래서 너가 `JOIN` 작성할 때 실제로는 `INNER JOIN`으로 작성된다.
```sql
SELECT Products.ProductID, Products.ProductName, Categories.CategoryName
FROM Products
JOIN Categories ON Products.CategoryID = Categories.CategoryID
```
## JOIN Three Tables
다음 SQL 문장은 모든 주문을 선택한다 커스터머 와 송장 정보와 같이
```sql
SELECT Orders.OrderID, Customers.CustomerName, Shippers.ShipperName
FROM ((Orders
INNER JOIN Customers ON orders.CustomerID = Customers.CustomerID)
INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID);
```
