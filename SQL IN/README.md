# SQL IN 연산자
## SQL IN 연산자
`IN`연산자를 사용하면 `WHERE`절에 여러 값을 지정할 수 있다.
`IN`연산자는 여러 개의 OR 조건을 나타내는 약어이다.
```sql
SELECT * FROM Customers WHERE Country IN ('Germany', 'France', 'UK');
```
## 문법
```sql
SELECT column_name(s) FROM table_name WHERE column_name IN (value1, value2, ...)
```
## NOT IN
`IN` 연산자의 앞에 `NOT`키워드를 사용하여, 어떤 값도 아닌 모든 레코드를 리턴한다.
```sql
SELECT * FROM Customers WHERE Country NOT IN ('Germany', 'France', 'UK');
```
## IN (SELECT)
`IN` 같이 `WHERE`절을 서브쿼리로 사용할 수 있다.
하위 쿼리를 사용하면 하위 쿼리 결과에 존재하는 주 쿼리의 모든 레코드를 반환할 수 있습니다.
```sql
SELECT * FROM Customers WHERE CustomerID IN (SELECT CustomerID FROM Orders);
```
## NOT IN (SELECT)
예제의 결과로 74레코드를 리턴하는데, 이 의미는 17 커스터머들은 어떤 주문도 하지 않았다.
```sql
SELECT * FROM Customers WHERE CustomerID NOT IN (SELECT CustomerID FROM Orders);
```

