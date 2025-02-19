# SQL SUM() 함수
## SQL SUM() 함수
`SUM()` 함수는 숫자 컬럼의 총 합을 리턴한다.
```sql
SELECT SUM(Quantity) FROM OrderDetails;
```
## 문법
```sql
SELECT SUM(column_name)
FROM table_name
WHERE condition;
```

## WHERE 절 추가
조건을 지정하기 위해 `WHERE` 절을 추가할 수 있다.
```sql
SELECT SUM(Quantity) FROM OrderDetails WHERE ProductId = 11;
```

## 별칭 사용
`AS` 키워드를 사용하여 요약된 열에 이름을 지정합니다.
```sql
SELECT SUM(Quantity) AS total FROM OrderDetails;
```

## SUM() GROUP BY와 같이 사용
여기서는 SUM() 함수와 GROUP BY 절을 사용하여 OrderDetails 테이블의 각 OrderID에 대한 수량을 반환합니다.
```sql
SELECT OrderID, SUM(Quantity) AS [Total Quantity]
FROM OrderDetails
GROUP BY OrderID;
```
## 표현식을 사용한 SUM()
SUM() 함수 내부의 매개변수는 표현식일 수도 있습니다. OrderDetails 열의 각 제품이 10달러라고 가정하면 각 수량에 10을 곱하여 총 수입을 달러로 구할 수 있습니다.
```sql
SELECT SUM(Quantity * 10)
FROM OrderDetails;
```
```sql
SELECT SUM(Price * Quantity)
FROM OrderDetails
LEFT JOIN Products ON OrderDetails.ProductID = Products.ProductID;
```



