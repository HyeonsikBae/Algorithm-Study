## 정수 제곱근 판별

언어 : Python

작성 : Byul Han

### 코드

```python
def solution(n):
    if n == 1 : return 4  # n이 1일때 범위 오류가 생겨 따로 값을 지정해줌
    for i in range(1, n // 2 + 1): 
    	if i == n / i:
        	return (i + 1) * (i + 1)
    return -1
```

range 값을 n // 2로 잘못설정했던 부분 수정

