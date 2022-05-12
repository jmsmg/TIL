# SQL 문법

## SELECT

- 모든 열 가져오기

```sql
SELECT * FROM Customers;
```

- 원하는 열만 가져오기

```sql
SELECT CustomerName, CustomerID FROM Customers;
```

```sql
SELECT CustomerName, 1, 'Hello', NULL
FROM Customers;
```

- 원하는 행만 가져오가

```sql
SELECT * FROM OrderDetails 
WHERE Quantity < 5;
```

- 원하는 순서(default 오름차순)

```sql
SELECT * FROM OrderDetails
ORDER BY ProductID ASC;
```

- 원하는 만큼 데이터 가져오기

```sql
SELECT * FROM Customers
ORDER BY CustomerID DESC
LIMIT 10;
```

- 칼럼명 변경

```sql
SELECT
  CustomerId AS ID,
  CustomerName AS NAME,
  Address AS ADDR
FROM Customers;
```

- 종합

```sql
SELECT
  CustomerID AS '아이디',
  CustomerName AS '고객명',
  City AS '도시',
  Country AS '국가'
FROM Customers
WHERE
  City = 'London' OR Country = 'Mexico'
ORDER BY CustomerName
LIMIT 0, 5;
```