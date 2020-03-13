
## 1
1. `SELECT COUNT(*) FROM EMP`
2. `SELECT COUNT(EMPNO) FROM EMP`
3. `SELECT COUNT(1) FROM EMP`
어떤 테이블(EMP)의 전체 Raw의 갯수를 구할려고 합니다. 세가지 Query문중 어떤 Query문이 제일 효율적인지 고르고 이유를 설명하시오.

---

## 2
KEEP 문을 사용하여 CUST_CREDIT_LIMIT의 최저 순위와 최고 순위를 구하여라 단 이때 CUST_CREDIT_LIMIT은 NULL 일 수 있습니다.

> DB : sh
> TABLE : CUNSTOMERS

---

## 3
CUST_CITY 별로 CUST_CREDIT_LIMIT의 랭킹을 구하시오. (동일 등수면 다음 수를 넘어가도록 설정)

> DB : sh
> TABLE : CUNSTOMERS
> 조건 : RANK, PATITION
