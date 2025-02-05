# SQL SELECT 문구
## SQL SELECT 문구
데이터베이스 에서 데이터를 선택하는데 사용된다.
```sql
SELECT CustomerName, City FROM Customers;
```
## 문법
```SQL
SELECT column1, column2, ... FROM table_name;
```
여기, column1, column2,...은 테이블 이름이다. 너가 선택할 데이타의
table_name은 너가 원하는 데이터의 테이블 이름을 표현한다.
### 모든 컬럼 추출
만약 너가 모든 컬럼을 얻고 싶으면, 모든 컬럼이름을 표현하지 않고, 단지 SELECT * 를 쓰면됨
```sql
SELECT * FROM Customers;
```
