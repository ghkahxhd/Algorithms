# Algorithms

## 정렬
정렬 문제는 다음과 같이 정의한다.
> 입력: 숫자 n개로 이루어진 수열 <a1, a2, ..., an>  
  출력: 입력 수열 <a'1, a'2, ..., a'n>을 a'1<=a'2<=...<=a'n의 순서로 재배치한 순열

 | 알고리즘  | 최악의 경우 수행시간 | 평균 / 기대 수행시간 |
 |----------|----------------------|----------------------|
 | 삽입 정렬 | Om(n^2)              | Om(n^2)              |
 | 병합 정렬 | Om(nlg(n))           | Om(nlg(n))           |
 | 힙 정렬   | O(nlg(n))            | -                    |
 | 퀵 정렬   | Om(n^2)              | Om(nlg(n)) (기대)    |
 | 계수 정렬 | Om(k+n)              | Om(k+n)              |
 | 기수 정렬 | Om(d(n+k))           | Om(d(n+k))           |
 | 버킷 정렬 | Om(n^2)              | Om(n) (평균)         |



 ## 2. 퀵 정렬
 ### 2.1 퀵 정렬

QUICKSORT(A, p, r)
```
if p < r
    q = PARTITION(A, p, r)
    QUICKSORT(A, p, q-1)
    QUICKSORT(A, q+1, r)
```

PARTITION(A, p, r)
```
x = A[r]
i = p-1
for j=p to r-1
    if A[j] <= x
        i = i+1
        A[i] <-> A[j] 교환
A[i+1] <-> A[r] 교환
return i+1
```
