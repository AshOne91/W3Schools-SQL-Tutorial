# SQL AVG() 함수
## SQL AVG() 함수
`AVG()`함수는 숫자열의 값의 평균을 리턴한다.
```sql
SELECT AVG(Price) FROM Products;
```
## 문법
```sql
SELECT AVG(column_name)
FROM table_name
WHERE condition;
```
## WHERE 절 추가
지정된 조건을 WHERE절에 추가할 수 있다.
```sql
SELECT AVG(Price)
FROM Products
WHERE CategoryID = 1;
```
## 별칭 사용
`AS`키워드를 사용해서 AVG 컬럼 이름을 주다.
```sql
SELECT AVG(Price AS [average price] FROM Products;
```

## 평균 보다 높은
평균보다 가격이 높은 모든 레코드를 나열하려면 하위 쿼리에서 `AVG()` 함수를 사용할 수 있습니다
```sql
SELECT * FROM Products WHERE price > (SELECT AVG(price) FROM Products);
```

## AVG()와같이 GROUP BY 사용
여기서는 `AVG()` 함수와 `GROUP BY` 절을 사용하여 Products 테이블의 각 범주에 대한 평균 가격을 반환합니다.
```sql
SELECT AVG(Price) AS AveragePrice, CategoryID
FROM Products
GROUP BY CategoryID;
```

