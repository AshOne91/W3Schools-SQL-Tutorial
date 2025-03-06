# SQL Self Join
## SQL Self Join
셀프 조인은 일반 조인이지만 테이블 자체가 자체적으로 조인됩니다.
## Self Join 문법
```sql
SELECT column_name(s)
FROM table1 T1, table1 T2
WHERE condition;
```
## SQL Self Join 예제
다음 SQL 문장은 같은 도시출신인 커스터머들을 매치해준다.
```sql
SELECT A.CustomerName AS CustomerName1, B.CustomerName AS CustomerName2, A.City
FROM CUstomers A, Customers B
WHERE A.CustomerID <> B.CustomerID
AND A.City = B.City
ORDER BY A.City;
```
