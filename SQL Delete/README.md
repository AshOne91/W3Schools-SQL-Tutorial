# SQL DELETE 문
## SQL DELETE 문
`DELETE`문은 테이블에서 존재하는 레코드를 삭제하는데 사용된다.
## DELETE 문
```sql
DELETE FROM table_name WHERE condition;
```
## SQL DELETE 예제
다음 SQL문은 커스터머 테이블에서 알프레드 커스터머를 삭제한다.
```sql
DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';
```
## 모든 레코드 삭제하기
테이블에 모든 행을 삭제 가능하다 테이블의 삭제없이. 이는 테이블 구조, 속성 및 인덱스가 그대로 유지됨을 의미한다.
```sql
DELETE FROM table_name;
```
다음 SQL 문은 커스터머에 모든 로우를 삭제한다., 테이블의 삭제 없이
```sql
DELETE FROM Customers;
```
## 테이블 삭제
테이블을 완벽히 삭제하기 위해, `DROP TABLE`문을 사용해라.
```sql
DROP TABLE Customers;
```


