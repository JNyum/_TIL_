# SQL 문법

## SQL Syntax
- SELECT 칼럼, 계산값
- FROM 테이블명
- WHERE 조건
- GROUP BY 그룹화
- HAVING 그룹화에 사용되는 조건

---

## SELECT
> 필요한 칼럼만 호출할 수 있다
``` SQL
SELECT 호출하려는 칼럼
FROM DB.TABLE;
```
**활용**
1. [집계 함수](https://docs.oracle.com/database/121/DWHSG/analysis.htm#DWHSG0203)
```SQL
SELECT 집계함수
FROM DB.TABLE;
```

1. 모든 결과 조회 (*)
```SQL
SELECT *
FROM DB.TABLE;
```

4. 여러 칼럼 조회 (,)
```SQL
SELECT 칼럼1, 칼럼2
FROM DB.TABLE;
```

5. 별칭 지정(AS)
```SQL
SELECT 칼럼 AS 별칭
FROM DB.TABLE;
```

6. 중복 제외 조회(DISTINCT)
```SQL
SELECT DISTINCT 칼럼
FROM DB.TABLE;
```

---

## FROM
> 테이블에 특정 정보를 호출하려면 쿼리에 테이블 명을 지정해주어야된다
```SQL
SELECT ~~
FROM DB.TABLE;
```

---

## WHERE
> 데이터를 조회할 때, 조건에 맞는 데이터만 조회할 수 있다
```SQL
SELECT 칼럼
FROM DB.TABLE
WHERE 조건;
```
**자주 사용되는 연산자**

1. BETWEEN
> BETWEEN 시작점 AND 끝점
```SQL
SELECT ~~
FROM DB.TABLE
WHERE 칼럼 BETWEEN 시작점 AND 끝점;
```

1. 대소관계   
> =, >, >=, <, <=, !=, <>
```SQL
SELECT ~~
FROM DB.TABLE
WHERE 칼럼 = 기준;
```

3. IN
> 칼럼의 값이 A이거나 B인 데이터 조회(A'또는' B인 데이터 출력)
```SQL
SELECT ~~
FROM DB.TABLE
WHERE 칼럼 IN (A, B);
```

4. NOT IN
> 칼럼의 값이 A, B가 아닌 데이터 조회
```SQL
SELECT ~~
FROM DB.TABLE
WHERE 칼럼 NOT IN (A, B);
```

5. IS NULL
> 값이 NULL인 데이터 조회
```SQL
SELECT ~~
FROM DB.TABLE
WHERE 칼럼 IS NULL;
```
6. IS NOT NULL
> 값이 NULL이 아닌 데이터 조회
```SQL
SELECT ~~
FROM DB.TABLE
WHERE 칼럼 IS NOT NULL;
```

7. LIKE
> 필드에 어떤 텍스트를 포함하는 데이터를 조회
```SQL
SELECT ~~
FROM DB.TABLE
WHERE 칼럼 LIKE %~~~%;
```

---

## GROUP BY
> 칼럼의 값들을 그룹화 할 수 있다   
> 주로 [집계함수](https://docs.oracle.com/database/121/DWHSG/analysis.htm#DWHSG0203)들과 함께 사용함
```SQL
SELECT 칼럼, 집계함수
FROM DB.TABLE
GROUP BY 그룹화 할 칼럼;
```

