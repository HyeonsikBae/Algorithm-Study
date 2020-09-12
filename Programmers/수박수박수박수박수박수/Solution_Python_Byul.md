## 수박수박수박수박수박수?

언어 : Python

작성 : Byul Han

### 코드 1

```python
def solution(n):
    watermelon = ''
    for i in range(n):
        if i % 2 == 0:
            watermelon += "수"
        else:
            watermelon += "박"
    # 0부터 n - 1 까지 교대로 수박을 이어붙여 그 값을 리턴함
    return watermelon
```

### 코드 2

```python
def solution2(n):
    return "".join(["수박"[i%2] for i in range(n)])
	# 수박이 번갈아 나오는 list를 만들어 join으로 합쳐줌
```

### 코드 3

```python
def solution3(n):
    s = "수박" * n
    return s[:n]
	# 수박을 n만큼 반복하여 원하는 길이만큼 리턴함
```

코드 3의 계산이 가장 빨랐고 str를 하나씩 가지는 list를 만들어 합치는 코드2가 가장 오래 걸림.