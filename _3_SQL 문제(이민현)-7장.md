## 1
**각 판매물품의 제품명, 제품가격, 판매일을 가져온다.
 대신 2000년 2월의 월요일과 금요일에만 판매된 제품을 가져오며, 가격 내림차순 정렬한다.**

> DB : sh  
> TABLE : COSTS, TIMES(필수아님)  
> 조건 : JOIN(필수아님), IN(필수아님), ORDER BY  

#### 결과
|PROD_NAME|UNIT_PRICE|TIME_ID|
|---------|----------|-------|
|Envoy Ambassador|1599|2000-02-25|
|Envoy Ambassador|1599|2000-02-25|
|Envoy Ambassador|1599|2000-02-07|
|Envoy Ambassador|1599|2000-02-07|
|Envoy Ambassador|1577|2000-02-21|
|Envoy Ambassador|1577|2000-02-14|
|Envoy Ambassador|1577|2000-02-14|
|Envoy Ambassador|1577|2000-02-21|
|Mini DV Camcorder with 3.5" Swivel LCD|1353|2000-02-25|
|Mini DV Camcorder with 3.5" Swivel LCD|1353|2000-02-25|
|Mini DV Camcorder with 3.5" Swivel LCD|1334|2000-02-21|
|Mini DV Camcorder with 3.5" Swivel LCD|1334|2000-02-21|
|17" LCD w/built-in HDTV Tuner|1301|2000-02-11|
|17" LCD w/built-in HDTV Tuner|1297|2000-02-28|

...
`총 459row`

---

## 2
**각 주문의 주문번호, 주문자의 Firstname, 주문건 내 물품중 조건에 맞는 물품의 개수를 가져온다.
온라인 구매건 주문내 물품중 200달러와 300달러 사이의 가격을 가진 물품의 개수를 가져온다.
해당하는 물품이 없으면 0으로 표시된다.**

> DB : oe  
> TABLE : ORDERS, ORDER_ITEMS, CUSTOMERS  
> 조건 : JOIN, BETWEEN, GROUP BY  

#### 결과
|ORDER_ID|CUST_FIRST_NAME|비싼 물품|
|--------|---------------|-----|
|2355|Harrison|1|
|2356|Matthias|0|
|2359|Matthias|2|
|2360|Matthias|0|
|2361|Meenakshi|1|
|2362|Christian|1|
|2363|Sivaji|0|
|2364|Mammutti|0|


...
`총 32row`

---

## 3
**직원의 firstname, 고용날짜, 월급, 그리고 해당 직원 부서의 부장의 firstname을 가져온다.
단 직원의 firstname은 e가 두개 포함되어 있으며, 고용날짜가 1987년이어야 한다. (LIKE 필수 사용)
또한 부장이 없을 경우, '없음'으로 표시한다.**

> DB : hr  
> TABLE : employees  
> 조건 : JOIN, LIKE, COALESCE(다른것 사용해도 됨)  

#### 결과
|first_name|hire_date|salary|부장|
|----------|---------|------|--|
|Steven|1987-06-17|24000.00|없음|
|Jennifer|1987-09-17|4400.00|Neena|



...
`총 2row`
