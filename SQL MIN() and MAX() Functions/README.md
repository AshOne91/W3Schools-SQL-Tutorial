# SQL MIN() 그리고 MAX() 함수들
## SQL MIN() 그리고 MAX() 함수들
`MIN()`함수는 선택된 컬럼의 가장 작은 값을 리턴한다.
`MAX()`함수는 선택된 컬럼의 가장 큰 값을 리턴한다.
```sql
SELECT MIN(Price) FROM Products;
```
```sql
SELECT MAX(Price) FROM Products;
```
## 문법
```sql
SELECT MIN(column_name) FROM table_name WHERE condition;
```
```sql
SELECT MAX(column_name) FROM table_name WHERE condition;
```
## 열 이름 설정(별칭)
`MIN()` 또는 `MAX()`을 사용할 때, 반환된 컬럼은 설명정인 이름을 가지고 있지 않을 것이다. 설명적인 이름을 주기 위해서는, `AS`키워드를 사용하라
```sql
SELECT MIN(Price) AS Smallest Price FROM Products;
```

## MIN() GROUP BY와 같이 사용하기
우리는 `MIN()`함수 그리고 `GROUP BY` 절을 사용할거야, 프로덕트 테이블에 각각의 카테고리의 최소 가격을 리턴받기 위해
```sql
SELECT MIN(Price) AS SmallestPrice, CategoryID FROM Products GROUP BY CategoryID;
```



