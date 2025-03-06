# The SQL UNION Operator
`UNION` 연산자는 두개 또는 그 이상 `SELECT`문장의 결과 집합 조합에 사용되어진다.
- `UNION`와 있는 모든`SELECT` 문은 컬럼들의 수가 무조건 동일해야 한다.
- 컬럼들은 비슷한 데이터 타입들을 가지고 있어야한다.
- 모든 `SELECT` 문장에 컬럼들은 같은 순서여야 한다.
## UNION Syntax
```sql
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2
```
## UNION ALL Syntax
`UNION` 연산자는 디폴트로 유일한 값만 선택한다. 중복값을 허락하기 위해, `UNION ALL` 사용
```sql
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2
```
결과 집합의 열 이름은 일반적으로 첫 번째 SELECT 문의 열 이름과 같습니다.
## SQL UNION Example
다음 SQL 문장은 도시들을 리턴한다. 양쪽 커스머 그리고 서플라이어 테이블로부터의 유일한 도시 값을
```sql
SELECT City FROM Customers
UNION
SELECT City FROM Suppliers
ORDER BY City;
```
## SQL UNION ALL With WHERE
다음 SQL 문은 도시가 독일인(중복 값 포함) 리턴한다. 양쪽 테이블에서
```sql
SELECT City, Country FROM Customers
WHERE Country='Germany'
UNION ALL
SELECT City, Country FROM Suppliers
WHERE COuntry='Germany'
ORDER BY City;
```
## Another UNION Example
다음 SQL 문장은 모든 커스터머 와 공급자를 리스트화 한다.
```sql
SELECT 'Customer' AS Type, ContactName, City, Country
FROM Customers
UNION
SELECT 'Supplier', ContactName, City, Country
FROM Suppliers;
```
