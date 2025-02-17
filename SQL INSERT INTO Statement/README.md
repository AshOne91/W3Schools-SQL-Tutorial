# SQL INSERT INTO 문
## SQL INSERT INTO 문
`INSERT INTO` 문은 테이블에 새로운 레코드를 삽입하는데 사용된다.
## INSERT INTO 문법
두가지 방법으로 `INSERT INTO` 문을 작성하는 것이 가능하다.
1. 삽입할 열 이름과 값을 모두 지정하라.
```sql
INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...);
```
2. 만약 너가 테이블의 모든 컬럼들에게 값을 추가한다면, SQL 쿼리에 컬럼이름을 명시할 필요가 없다. 그러나, 값의 순서가 표의 열 순서와 동일한지 확인하라. 여기, `INSERT INTO` 문법은 다음과 같다.
```sql
INSERT INTO table_name VALUES (value1, value2, value3, ...)
```

## INSERT INTO 예제
다음 SQL 문은 커스터머스 테이블에 새로운 레코드를 삽입한다.
```sql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');
```
## 지정된 컬럼에 만 데이터 삽입
지정된 컬럼에만 데이터를 삽입하는 것은 가능합니다.
다음 SQL문은 새로운 레코드를 삽입한다. 그러나 오직 커스터머이름, 시티, 그리고 컨트리 컬럼들에만 삽입한다.(커스터머아이디는 자동으로 업데이트 된다.)
```sql
INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');
```

## 다수의 행들 삽입
또한 하나의 문장에 다수의 행 삽입이 가능하다.
데아터의 다수의 행을 삽입하기 위해, 우리는 같은 `INSERT INTO`문장 사용한다. 그러나 다수의 값들을 같이
```sql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES
('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway'),
('Greasy Burger', 'Per Olsen', 'Gateveien 15', 'Sandnes', '4306', 'Norway'),
('Tasty Tee', 'Finn Egan', 'Streetroad 19B', 'Liverpool', 'L1 0AA', 'UK');
```




