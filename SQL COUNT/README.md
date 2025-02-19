# SQL COUNT() 함수
## SQL COUNT() 함수
`count()` 함수는 지정된 조건과 일치하는 행의 수를 리턴한다.
```sql
SELECT COUNT(*) FROM Products;
```
## 문법
```sql
SELECT COUNT(column_name) FROM table_name WHERE condition;
```

## 명시된 컬럼
컬럼 이름을 명시할 수 있다. asterix 심볼 대신에
만약 `(*)`대신에 이름을 명시하면, NULL 값들은 카운팅 되지 않을거다.
```sql
SELECT COUNT(ProductName) FROM Products;
```

## WHERE 절 추가
`WHERE`절에 지정된 조건을 추가할 수 있다.
```sql
SELECT COUNT(ProductID) FROM Products WHERE Price > 20;
```

## 중복 무시
중복을 제거할 수 있다 `DISTINCT`키워드로 `COUNT()`안에
만약 `DISTINCT`을 지정하면, 행들은 명시된 컬럼을 카운트할거다 하나로 같은 값에 대해서
```sql
SELECT COUNT(DISTINCT Price) FROM Products;
```

## 명칭 사용하기
카운트된 컬럼에 이름을 주기위해 `AS`키워드를 사용하라
```sql
SELECT COUNT(*) AS [Number of records] FROM Products;
```

## COUNT() GROUP BY와 같이 사용하기
`COUNT()`함수와 `GROUP BY`절을 여기 사용하다, 프로덕트 테이블에 각각의 카테고리에 레코드의 수를 리턴하기 위해
```sql
SELECT COUNT(*) AS [Number of records], CategoryID FROM Products GROUP BY CategoryID;
```
