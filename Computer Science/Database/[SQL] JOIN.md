## 1. Join 조인이란?

두 개 이상의 테이블을 연결해서 데이터를 검색하는 방법

## 2. 종류

### 1. INNER JOIN


```sql
SELECT
A.NAME, B.AGE
FROM EX_TABLE A
INNER JOIN JOIN_TABLE B ON A.NO_EMP = B.NO_EMP
```

기준 테이블과 join 테이블의 중복된 값 조회 `교집합`

⇒ 일치하는 값이 없는 행은 조회 X

<br>

### 2. OUTER JOIN

테이블 간에 JOIN시 일치하지 않는 행도 포함시켜서 조회 가능

- LEFT OUTER JOIN


```sql
SELECT
A.NAME, B.AGE
FROM EX_TABLE A
LEFT OUTER JOIN JOIN_TABLE B ON A.NO_EMP = B.NO_EMP
```

왼쪽 테이블에 있는 값 전부 조회됨

- RIGHT OUTER JOIN

```sql
SELECT
A.NAME, B.AGE
FROM EX_TABLE A
RIGHT OUTER JOIN JOIN_TABLE B ON A.NO_EMP = B.NO_EMP
```

오른쪽 테이블에 있는 값 전부 조회됨

- FULL OUTER JOIN


```sql
SELECT
A.NAME, B.AGE
FROM EX_TABLE A
FULL OUTER JOIN JOIN_TABLE B ON A.NO_EMP = B.NO_EMP
```

A와 B 테이블의 모든 데이터 조회됨 `합집합`

<br>

### 3. SELF JOIN

자기자신을 조인하는 것

```sql
SELECT
A.NAME, B.AGE
FROM EX_TABLE A, EX_TABLE B
```

<br>

### 4. CROSS JOIN

모든 테이블의 각 행들이 서로 곱해진 데이터 조회됨 `곱집합`

```sql
SELECT
A.NAME, B.AGE
FROM EX_TABLE A
CROSS JOIN JOIN_TABLE B
```
