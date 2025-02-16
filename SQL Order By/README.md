# SQL ORDER BY 키워드
## SQL ORDER BY
`ORDER BY` 키워드는 결과를 오름차순 혹은 내림차순 정렬하는데 사용되어 진다.
```sql
SELECT * FROM products ORDER BY Price;
```
## 문법
```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```
## DESC
`ORDER BY`키워드는 기본적으로 오름차순으로 레코드를 정렬한다. 내림차순으로 정렬하기 위해서는, `DESC`키워드를 사용해라.
```sql
SELECT * FROM Products
ORDER BY price DESC;
```
## 알파벳순 정렬
문자열값들의 `ORDER BY` 키워드는 알파벳순으로 정렬한다.
```
SELECT * FROM products ORDER By productName;
```

## 알파벳순 내림차순
다음 SQL문은 커스터머 테이블의 모든 커스터머들, 컨트리 그리고 커스터머이름 순으로 정렬 선택한다. 이것은 이미한다. 컨트리 순으로 정렬하는것을, 그러나 만약 몇몇의 행은 같은 컨트리를 가지고 있어서, 그것을 커스터머이름 순으로 정렬한다.
```sql
SELECT * FROM Customers ORDER BY Country, CustomerName;
```

## 오름차순, 내림차순 동시에 사용하기
다음 SQL문은 커스터머테이블에서 모든 커스터머를 선택한다. 컨트리 순으로 정렬하고 커스터머 이름으로 내림차순 한다.
```sql
SELECT * FROM Customers ORDER BY Country ASC, CustomerName DESC;
```





