# SQL SELECT DISTINCT 문구
## THE SQL SELECT DISTINCT 문구
'SELECT DISTINCT' 문구는 오직 다른 값만 리턴하는데 사용된다.
```sql
SELECT DISTINCT Contry FROM Customers;
```
테이블 안에, 컬럼은 종종 많은 중복된 값을 담고있다; 그리고 가끔 너는 오직 원한다 다른 값을 리스트하는것을

## 문법
```sql
SELECT DISTINCT column1, column2, ... FROM table_name;
```

## 유일값 카운트
'DISTINCT'키워드를 함수 안에서 사용하기 위해 'COUNT'를 콜하기, 우리는 각각 구역의 수를 돌려 받을수 있다.
```sql
SELECT COUNT(DISTINCT Contry) FROM Customers;
```
위의 함수는 MAD에서는 지원하지 않는다.
MA Access에서 사용하기 위해서는
```sql
SELECT Count(*) AS DistinctContries
FROM (SELECT DISTINCT COntry FROM Customers);
```
카운트 함수에 대해 이후 튜토리얼에서 배울거다.^^
