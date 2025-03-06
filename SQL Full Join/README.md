# SQL FULL OUTER JOIN Keyword
## SQL FULL OUTER JOIN Keyword
`FULL OUTER JOIN` 키워드는 모든 레코드를 리턴한다. 왼쪽 테이블 또는 오른쪽 테이블 레코드가 매치될 때
`FULL OUTER JOIN`과 `FULL JOIN`은 같다.
## FULL OUTER JOIN 문법
```sql
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```
## SQL FULL OUTER JOIN Example
```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
```
`FULL OUTER JOIN`키워드는 모든 매칭된 레코드들을 리턴한다 양쪽 테이블로부터 다른 매치되지 않아도, 그래서 만약 커스터머에서 주문이 매치되지 않아도, 또한 만약 커스터머에 주문이 매치되지 않아도, 그것들 또한 리스트화 될거다.
