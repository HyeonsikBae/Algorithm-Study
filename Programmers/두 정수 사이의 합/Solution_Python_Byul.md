## 두 정수 사이의 합

언어 : Python

작성 : Byul Han

### 코드

```python
def solution(a, b):
    answer = 0
    if a == b:
        return a
    # a와 b가 같은 경우 a 리턴, b를 리턴해도 무방하다
    elif a > b:
        for i in range(b, a + 1):
            answer += i
    else:
        for i in range(a, b + 1):
            answer += i
    # a와 b의 대소관계를 구분해 범위 설정 후 answer에 반복문으로 더해준다
    return answer
```

### 다른 풀이

```python
def solution(a, b):
   return sum(i for i in range(min(a, b), max(a, b) + 1))
```

대소관계 비교를 min과 max를 이용해 보다 간결하게 풀어봄.

밑의 코드가 계산 속도도 조금 더 빠른 것을 확인함.

