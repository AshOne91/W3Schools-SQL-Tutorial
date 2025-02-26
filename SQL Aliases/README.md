# SQL Aliases
## SQL 별칭
SQL 별칭은 테이블에 주는데 사용되어진다. 테이블에 컬럼, 임시 이름
별칭은 종종 컬럼의 이름을 읽기좋게 만들어 주는데 사용되어진다.
별칭은 오직 존재한다 쿼리의 기간동안만
별칭은 만들어진다 `AS`키워드와 같이
```sql
SELECT CustomerID AS ID FROM Customers;
```
## AS is Optional
실제로, 대부분의 데이터베이스 언어에서, 너는 AS 키워드를 스킵해도 같은 결과를 얻을수 있다.
```sql
SELECT CustomerID ID FROM Customers;
```
## 문법
```sql
SELECT column_name AS alias_name FROM table_name;
```
## 컬럼의 별칭들
다음 SQL 문장은 두개의 명칭을 생성한다, 커스터머아이디 컬럼 하나와 커스터머이름 하나
```sql
SELECT CustomerID AS ID, CustomerName AS Customer FROM Customers;
```
## 공백 문자와 같이 별칭 사용하기
별칭에 하나 혹은 그 이상의 공백을 원한다면, "`My Greate Products1`"처럼, 너의 별칭을 네모 괄호 또는 쌍다옴표로 감싸라
```sql
SELECT ProductName AS [My Greate Products] FROM Products;
```
```sql
SELECT ProductName AS "My Greate Products" FROM Products;
```
## 컬럼 연결
다음 SQL 문은 열들의 조합을 "Address"로 네이밍하여 생성한다.
```sql
SELECT CustomerName, Address + ', ' + PostalCode + ' ' + City + ', ' + Country AS Address
FROM Customers;
```
Note: To get the SQL statement above to work in MySQL use the following:
```sql
SELECT CustomerName, CONCAT(Address,', ',PostalCode,', ',City,', ',Country) AS Address
FROM Customers;
```
Note: To get the SQL statement above to work in Oracle use the following:
```sql
SELECT CustomerName, (Address || ', ' || PostalCode || ' ' || City || ', ' || Country) AS Address
FROM Customers;
```
## Alias for Tables
The same rules applies when you want to use an alias for a table.
```sql
SELECT * FROM Customers AS Persons;
```
테이블의 별칭은 필요가 없어 보이지만 너가 하나 이상의 테이블을 쿼리에서 사용할 때 SQL문장을 짧게하는 것이 가능하다.
다음 SQL 문장은 모든 주문을 선택한다 커스터머로 부터 ~~
```sql
SELECT o.OrderID, o.OrderDate, c.CustomerName
FROM Customers AS c, Orders AS o
WHERE c.CustomerName='Around the Horn' AND c.CustomerID=o.CustomerID;
```
다음 sql문장은 위와 같다, 그러나 별칭을 사용하지는 않음
```sql
SELECT Orders.OrderID, Orders.OrderDate, Customers.CustomerName
FROM Customers, Orders
WHERE Customers.CustomerName='Around the Horn' AND Customers.CustomerID=Orders.CustomerID;
```
