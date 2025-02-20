# SQL LIKE 연산자
## SQL LIKE 연산자
`LIKE`연산자는 `WHERE`절에서 사용되어진다 컬럼에서 지정된 패턴을 검색하기 위해
두개의 와일드카드가 사용되어진다 접속사로 `LIKE` 연산자와 함께
- 퍼센트 기호 `%`는 표현한다 제로, 하나, 또는 다수의 문자들
- 언더스코어 기호 `_`는 표현한다 하나, 싱글 문자를
```sql
SELECT * FROM Customers WHERE CustomerName LIKE 'a%';
```
## 문법
```sql
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```
## _ 와일드카드

`_`와이드카드는 표현한다 싱글 캐릭터를.
어느 캐릭터 또는 숫자일 수 있다, 그러나 각 `_`표현한다 하나, 혹은 유일한 하나, 캐릭터
```sql
SELECT * FROM Customers WHERE city LIKE 'L_nd__';
```

## % 와일드카드
The `%`와이들카드는 표현한다 다수의 캐릭터들을, 심지어 제로 캐릭터들도
```sql
SELECT * FROM Customers WHERE city LIKE '%L%';
```
또한 `AND`또는`OR`연산자들을 사용하여 다수의 조건을 조합할수 있다.
```sql
SELECT * FROM Customers WHERE CustomerName LIKE 'a%' OR CustomerName LIKE 'b%';
```
## Ends With
문장 혹은 절로 끝나는 레코드를 리턴받기 위해, `%`를 문장 혹은 시작의 처음부분에 추가하라
```sql
SELECT * FROM Customers WHERE CustomerName LIKE '%a';
```
Tip: You can also combine "starts with" and "ends with":
```sql
SELECT * FROM Customers WHERE CustomerName LIKE 'b%s';
```

## 포함하다.
특정 문자나 문구가 포함된 레코드를 반환하려면 해당 문자나 문구의 앞과 뒤에 %를 추가합니다.
```sql
SELECT * FROM Customers WHERE CustomerName LIKE '%or%';
```

## 와일드카드 조합
`%` 및 `_`와 같은 모든 와일드카드는 다른 와일드카드와 함께 사용할 수 있습니다.
```sql
SELECT * FROM Customers WHERE CustomerName LIKE 'a__%';
```
## 와일드카드 없이
와일드카드가 지정되지 않으면 구문과 정확하게 일치해야 결과가 반환됩니다.
```sql
SELECT * FROM Customers WHERE Country LIKE 'Spain';
```



