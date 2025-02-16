# SQL AND 연산자
## SQL AND 연산자
`WHERE` 절은 하나 또는 많은 `AND`연산자들을 포함할 수 있다.
`AND`연산자는 레코드 필터로 사용되어진다. 하나 혹은 하나 이상의 조건에, 만약 스페인에 거주중이고 이름 첫글자가 'G'인 모든 커스터머를 리턴받고 싶을때
```sql
SELECT * FROM Customers WHERE Country = 'Spain' AND CustomerName LIKE 'G%'
```
## 문법
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```
## AND vs OR
`AND` 연산자는 모든 조건이 TRUE인 경우 레코드를 표시합니다. 
`OR` 연산자는 조건 중 하나라도 TRUE인 경우 레코드를 표시합니다.

## 모든 조건이 참이어야 합니다
다음 SQL 문은 Country가 "Germany"이고 City가 "Berlin"이고 PostalCode가 12000보다 큰 Customers의 모든 필드를 선택합니다.
```sql
SELECT * FROM Customers
WHERE Country = 'Germany'
AND City = 'Berlin'
AND PostalCode > 12000;
```

## AND 그리고 OR 조합하기
`AND` 그리고 `OR` 연산자들은 조합이 가능합니다.
다음 SQL문은 지역이 Spain 이고 첫글자가 "G" 또는 "R"인 모든 커스터머들을 선택합니다.
올바른 결과를 얻기 위해서 괄호를 사용해야 한다.
```sql
-- Select all Spanish customers that starts with either "G" or "R":

SELECT * FROM Customers WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');
```

괄호 없이, select 문구는 지역이 Spain이고 첫글자가 "G'인 커스터머들, 거기다 첫글자가 "R"인 모든 커스터머들의 결과를 받을것이다. 지역과 상관없이
```sql
SELECT * FROM Customers WHERE Country = 'Spain' AND CustomerName Like 'G%' OR CustomerName LIKE 'R%';
```




