# SQL OR Operator
## SQL OR 연산자
`WHERE`절은 하나 또는 많은 `OR` 연산자들을 포함하고 있다.
`OR` 연산자는 레코드의 필터로 사용된다. 만약 너가 결과를 원한다 모든 커스터머들 독일 또는 스페인
```sql
SELECT *
FROM Customers
WHERE Country = 'Germany' OR Country = 'Spain';
```
## 문법
```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3...;
```

## OR vs AND
`OR` 연산자는 조건 중 하나라도 TRUE이면 레코드를 표시합니다. 
`AND` 연산자는 모든 조건이 TRUE이면 레코드를 표시합니다.

## 최소 하나의 조건이 참이여야 함
다음 SQL 문은 시티가 베를린이거나 커스터머이름 첫글자가 "G" 또는 컨트리가 Norway인 모든 필드를 선택한다.
```sql
SELECT * FROM Customers WHERE City = 'Berlin' OR CustomerName LIKE 'G%' OR Country = 'Norway';
```

## AND 그리고 OR 조합하기
`AND` 그리고 `OR` 연산자들을 조합할 수 있다.
다음 SQL문은 첫글자가 "G" 또는 "R"인 모든 스페인 커스터머를 선택한다.
올바른 게 괄호를 사용해야 한다. 올바른 결과를 얻기위해
```sql
SELECT * FROM Customers WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');
```

괄호가 없으면, 지역이 스페인이고 첫글자가 "G", 추가로 첫글자가 "R"인 모든 커스터머가 포함되어 결과를 받는다. 컨트리 값과 관계없이
```sql
SELECT * FROM Customers WHERE Country = 'Spain' AND CustomerName LIKE 'G%' OR CustomerName LIKE 'R%';
```
