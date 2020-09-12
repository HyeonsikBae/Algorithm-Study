## 콜라츠 추측

언어 : Python 

작성 : Byul Han

### 코드

```python
def solution(n):
    for i in range(0, 500): # 500번 반복으로 위해 0부터 499까지 범위설정
        if n == 1:
            return i # n이 1이 될때의 회차를 리턴
        elif n % 2 == 0:
            n /= 2
        else:
            n = n * 3 + 1
    return -1
```

### 코드 2

```python
def solution(n):
    answer = 0
    while answer < 500: # 반복문만 다르게 적용
        if n == 1:
            return answer
        elif n % 2 == 0:
            n = n / 2
        else:
            n = n * 3 + 1
        answer += 1
    return -1
```

