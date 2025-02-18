# SQL TOP, LIMIT, FETCh FIRST or ROWNUM 절
## SQL SELECT TOP 절
`SELECT TOP` 절은 반환할 레코드 수를 지정하는 데 사용된다.
`SELECT TOP` 절은 수천 개의 레코드가 있는 대형 테이블에서 유용합니다. 많은 수의 레코드를 반환하면 성능에 영향을 줄 수 있습니다.
```sql
-- Select only the first 3 records of the Customers table:
SELECT TOP 3 * FROM Customers;
```
Note: Not all database systems support the SELECT TOP clause. MySQL supports the LIMIT clause to select a limited number of records, while Oracle uses FETCH FIRST n ROWS ONLY and ROWNUM.
```sql
SQL Server / MS Access Syntax:

SELECT TOP number|percent column_name(s)
FROM table_name
WHERE condition;

MySQL Syntax:

SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number;

Oracle 12 Syntax:

SELECT column_name(s)
FROM table_name
ORDER BY column_name(s)
FETCH FIRST number ROWS ONLY;

Older Oracle Syntax:

SELECT column_name(s)
FROM table_name
WHERE ROWNUM <= number;

Older Oracle Syntax (with ORDER BY):

SELECT *
FROM (SELECT column_name(s) FROM table_name ORDER BY column_name(s))
WHERE ROWNUM <= number;
```

## LIMIT
다음 SQL 문은 MySQL에 대한 동등한 예를 보여줍니다.
```sql
Select the first 3 records of the Customers table:

SELECT * FROM Customers
LIMIT 3;
```

## ADD the ORDER BY Keyword
```sql
The following SQL statement shows the equivalent example for MySQL:

Example
SELECT * FROM Customers
ORDER BY CustomerName DESC
LIMIT 3;
```
