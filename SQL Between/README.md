# SQL BETWEEN 연산자
## SQL BETWEEN 연산자
`BETWEEN` 연산자는 주어진 범위안에 값들을 선택한다. 그 값들은 숫자, 문자 또는 날짜가 가능하다.
`BETWEEN` 연산자는 포함한다 : 시작부터 끝까지의 값들을 포함한다.
```sql
SELECT * FROM Products WHERE Price BETWEEN 10 AND 20;
```
## 문법
```sql
SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value1 AND value2;
```
## NOT BETWEEN
이전 예제의 범위 밖의 상품을 표시하기 위해, `NOT BETWEEN`을 사용한다.
```sql
SELECT * FROM Products WHERE Price NOT BETWEEN 10 AND 20;
```
## BETWEEN with IN
다음의 SQL문은 가격이 10 그리고 20사이, 추가적으로, 카테고리아이디가 1, 2, 또는 3인 물픔들을 선택한다.
```sql
SELECT * FROM Products WHERE Price BETWEEN 10 AND 20 AND CategoryID IN (1, 2, 3);
```

## BETWEEN Text Values
다음의 SQL문은 모든 상품을 선택한다 프로덕트이름 알파벳순으로 카나본 타이버 그리고 모짤레라 디 지오반니 사이에
```sql
SELECT * FROM Products WHERE ProductName BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni' ORDER BY ProductName;
```

## NOT BETWEEN Text Values
다음 SQL문은 모든 상품을 선택한다 프러덕트이름이 위 예제의 밖의 범위에
```sql
SELECT * FROM Products WHERE ProductName NOT BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni' ORDER BY ProductName;
```

## BETWEEN Dates
다음 SQL문은 모든 주문을 선택한다 OrderDate 사이에 '01-July-1996' and '31-July-1996':
```sql
SELECT * FROM Orders WHERE OrderDate BETWEEN #07/01/1996# AND #07/31/1996#;
```
또는
```sql
SELECT * FROM Orders WHERE OrderDate BETWEEN '1996-07-01` AND `1996-07-31`;
```
