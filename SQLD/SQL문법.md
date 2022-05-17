# SQL 문법

## SELECT 전반 기능

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

## SELECT 연산자

- 사칙연산

```sql
SELECT 5 - 2.5 AS DIFFERENCE;
```

- 문자열에 사칙연산을 가하면 문자열을 0으로 인식
  - 문자열 안에 숫자는 자동으로 인식함

```sql
SELECT '1' + '002' * 3;

-- 숫자로 구성된 문자열은 숫자로 자동인식
```

```sql
SELECT
  OrderID + ProductID
FROM OrderDetails;
```

```sql
SELECT
  ProductName,
  Price / 2 AS HalfPrice
FROM Products;
```

- 참/거짓

## SELECT 숫자와 문자

- 숫자 관련 함수

```sql
SELECT
  ROUND(0.5),
  CEIL(0.4),
  FLOOR(0.6);
```

```sql
SELECT 
  Price,
  ROUND(price),
  CEIL(price),
  FLOOR(price)
FROM Products;
```

## SELECT 시간/날짜

## SELECT 조건에 따라 그룹으로 묶기