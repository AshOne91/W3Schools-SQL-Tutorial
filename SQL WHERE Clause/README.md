# SQL WHERE 절
## THE SQL WHERE 절
'WHERE' 절은 레코드 필터에 사용된다.
지정된 조건을 충족하는 레코드만 추출하는 데 사용된다.
```sql
SELECT * FROM Customers
WHERE Contry='Mexico';
```
## 구문
```sql
SELECT column1, column2, ... FROM table_name WHERE condition;
```
노트 : 'WHERE'절은 'SELECT'에서만 사용되어지는 것이 아니다. 그것은 또한 사용되어진다... UDATE, DELETE, etc...
## 텍스트 필드 vs 숫자 필드
SQL은 작은 따옴표를 텍스트에 감싸는걸 요구한다. 그러나 숫자는 그렇지 않다.
```sql
SELECT * FROM Customers WHERE CustomerID=1;
```
## WHERE절의 연산자
'='대신 다른 연산자를 사용가능하다.
```sql
SELECT * FROM Customers WHERE CustomerID > 80;
```

Operator	Description	Example
| Operator  | Description                            | Example |
|-----------|----------------------------------------|---------|
| =         | Equal                                 |         |
| >         | Greater than                          |         |
| <         | Less than                             |         |
| >=        | Greater than or equal                 |         |
| <=        | Less than or equal                    |         |
| <>        | Not equal. Note: In some versions of SQL this operator may be written as != |         |
| BETWEEN   | Between a certain range              |         |
| LIKE      | Search for a pattern                 |         |
| IN        | To specify multiple possible values for a column |         |


