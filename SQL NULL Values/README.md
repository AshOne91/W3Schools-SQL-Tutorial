# SQL NULL 값들
## NULL 값이란 무엇인가?
NULL 값을 갖는 필드는 값이 없는 필드이다.
만약 테이블에 필드가 선택사항이면, 새로운 레코드 그리고 레코드의 갱신이 가능하다. 새로운 필드값의 추가 없이, 그리고 필드는 저장될거다 NULL value와 같이
## NULL 값을 테스트하는 방법?
비교 연산자를 사용하여 NULL 값을 테스트하는 것은 불가능하다, =, <, 그리고 <> 같이.
우리는 연산자 대신에 `IS NULL` 그리고 `IS NOT NULL`를 사용해야 된다.
## IS NULL 문법
```sql
SELECT column_names
FROM table_name
WHERE column_name IS NULL;
```
## IS NOT NULL 문법
```sql
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
```
## IS NULL 연산자
`IS NULL`연산자는 비어있는 값을 위해 테스트하는데 사용되어 진다.
다음 SQL은 "주소" 필드에 NULL 값이 있는 모든 고객을 나열합니다.
```sql
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;
```

## IS NOT NULL 연산자
`IS NOT NULL` 연산자는 비어 있지 않은 값(NOT NULL 값)을 테스트하는 데 사용되어 진다.
다음 SQL은 "주소" 필드에 값이 있는 모든 고객을 나열합니다
```sql
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NOT NULL;
```
