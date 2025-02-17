# SQL UPDATE 문
## SQL UPDATE 문
`UPDATE`문은 테이블에 존재하는 레코드의 수정에 사용되어 진다.
## UPDATE 문법
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```
## UPDATE 테이블
다음 SQL 문은 첫 번째 고객(CustomerID = 1)을 새 담당자와 새 도시로 업데이트합니다.
## UPDATE 다수의 레코드
`WHERE` 절은 어떤 레코드들을 업데이트할것인지 결정한다.
다음 SQL문은 컨트리가 멕시코인 모든 레코드들의 컨텍트네임을 주안으로 업데이트할것이다.
```sql
UPDATE Customers
SET ContactName='Juan'
WHERE Country='Mexico';
```
## Update Warning!
레코드를 업데이트할 때 주의하라. 만약 `WHERE`를 생략하면, 모든 레코드는 업데이트된다.
```sql
UPDATE Customers
SET ContactName='Juan';
```

