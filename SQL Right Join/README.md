# SQL RIGHT JOIN 키워드
## SQL RIGHT JOIN 키워드
`RIGHT JOIN` 키워드는 모든 레코드들을 반환한다 오른쪽 테이블로부터, 그리고 왼쪽 테이블로부터 매칭된 레코드들을
만약 매치되지 않으면 왼쪽 사이드로부터0개의 레코드가 결과다
## RIGHT JOIN Syntax
```sql
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```
## SQL RIGHT JOIN 예제
다음 SQL 문장은 모든 employees를 리턴한다, 그리고 그들이 내린 어느 주문들도
```sql
SELECT Orders.OrderID, Employees.LastName, Employees.FirstName
FROM Orders
RIGHT JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY Orders.OrderID;
```
