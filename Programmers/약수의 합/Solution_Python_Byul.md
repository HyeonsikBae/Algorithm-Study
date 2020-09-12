## 약수의 합

언어 : Python

작성 : Byul Han

### 코드

```python
def solution(n):
    answer = 0
    for i in range(1, n + 1):
        if n % i == 0:
            answer += i
    # n까지의 범위중에 나눠지는 값을 더해서 리턴
    return answer
```

### 수정 코드

```python
def solution(n):
    answer = 0
    for i in range(1, n // 2 + 1): 
        # 약수는 주어진 값의 절반값 이상이 될 수 없으므로 n // 2 + 1 로 반복 범위를 줄임
        if n % i == 0:
            answer += i
    return answer + n # 자기 자신을 약수로 가지기 때문에 범위에서 제외된 n을 더해서 리턴
```

