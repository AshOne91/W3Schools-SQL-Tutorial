# SQL NOT 연산자
## NOT 연산자
`NOT` 연산자는 조합에 사용되어진다 다른 연산자와 같이 반대되는 결과를 얻기 위해, 또한 불려진다 반대되는 결과를.
아래 select 문구에서 우리는 모든 커스터머의 결과를 원한다 스페인에 살지 않는
```sql
SELECT * FROM Customers
WHERE NOT Country = 'Spain';
```
예제에 따르면, `NOT`연산자는 조합에 사용된다 `=`연산자와 같이, 그러나 그것은 조합에 사용할거다 다른 표현식 and/or 흐름 연산자들, 아래 예제를 보자
## 문법
```sql
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```
## NOT LIKE
Select customers that does not start with the letter 'A':
```
SELECT * FROM Customers
WHERE CustomerName NOT LIKE 'A%';
```
## NOT BETWEEN
Select customers with a customerID not between 10 and 60:
```sql
SELECT * FROM Customers
WHERE CustomerID NOT BETWEEN 10 AND 60;
```
## NOT IN
Select customers that are not from Paris or London:
```sql
SELECT * FROM Customers
WHERE City NOT IN ('Paris', 'London');
```
## NOT Greater Than
Select customers with a CustomerId not greater than 50:
```sql
SELECT * FROM Customers
WHERE NOT CustomerID > 50;
```
## NOT Less Than
Select customers with a CustomerID not less than 50:
```sql
SELECT * FROM Customers
WHERE NOT CustomerId < 50;
```
