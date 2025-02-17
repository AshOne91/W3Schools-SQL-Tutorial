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



