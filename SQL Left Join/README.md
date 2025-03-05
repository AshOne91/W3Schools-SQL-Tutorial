# SQL LEFT JOIN Keyword
## SQL LEFT JOIN Keyword
`LEFT JOIN` 키워드는 왼쪽 테이블(table1) 부터 모든 레코드를 리턴받는다, 그리고 매칭된 레코드들 오른쪽 테이블(table2)부터. 만약 매치되지 않으면 0 레코드들을 오른쪽 사이드로부터 반환된다.
## LEFT JOIN 문법
```sql
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```
## SQL LEFT JOIN 예제
```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
```
Note: `LEFT JOIN` 키워드는 모든 레코드를 반환한다. 왼쪽 테이블을 심지어 오른쪽 테이블에 매치되지 않아도
