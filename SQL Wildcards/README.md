# SQL 와일드카드들
## SQL 와일드카드 문자들
와일드카드 문자는 문자열에서 하나 이상의 문자를 대체하는 데 사용된다.
와일드카드 문자들은 사용되어진다 `LIKE`연산자와. `LIKE`연산자는 사용되어진다 `WHERE`절에서 지정된 패턴을 컬럼에서 검색하기위해
```sql
SELECT * FROM Customers WHERE CustomerName LIKE 'a%';
```
Wildcard Characters
Symbol	Description
%	Represents zero or more characters
_	Represents a single character
[]	Represents any single character within the brackets *
^	Represents any character not in the brackets *
-	Represents any single character within the specified range *
{}	Represents any escaped character **
* Not supported in PostgreSQL and MySQL databases.
** Supported only in Oracle databases.
  
## % 와일드카드 사용하기
`%`와일드카드는 다수의 문자를, 심지어 제로 문자도 표현한다.
```sql
SELECT * FROM Customers WHERE CustomerName LIKE '%es';
```
```sql
SELECT * FROM Customers WHERE CustomerName LIKE '%mer%';
```

## _ 와일드카드 사용하기
`_`ㅇ와일드카드는 싱글문자를 표현한다.
문자나 숫자가 될수있다, 그러나 각각의 `_`표현한다 하나, 또는 오직한개, 문자.
```sql
SELECT * FROM Customers WHERE City LIKE '_ondon';
```
```sql
SELECT * FROM Customers WHERE City LIKE 'L___on';
```

## [] 와일드카드 사용하기
[] 와일드카드는 내부의 문자 중 하나라도 일치하는 경우 결과를 반환합니다.
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '[bsp]%';
```
## Using the `-` Wildcard

The `-` wildcard allows you to specify a range of characters inside the `[]` wildcard.

## Example  
Return all customers starting with "a", "b", "c", "d", "e" or "f":

```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '[a-f]%';
```

---

## Combine Wildcards

Any wildcard, like `%` and `_`, can be used in combination with other wildcards.

## Example  
Return all customers that start with "a" and are at least 3 characters in length:

```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'a__%';
```

## Example  
Return all customers that have "r" in the second position:

```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '_r%';
```

---

## Without Wildcard

If no wildcard is specified, the phrase has to have an exact match to return a result.

## Example  
Return all customers from Spain:

```sql
SELECT * FROM Customers
WHERE Country LIKE 'Spain';
```





