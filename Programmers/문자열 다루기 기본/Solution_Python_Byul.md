## 문자열 내림차순으로 배치하기

언어 : Python

작성 : Byul Han

### 코드1

```python
def solution(s):
    return s.isdigit() and len(s) in (4, 6)
	# 길이가 4 또는 6이고 숫자로 이뤄진 문자열인지 판단하여 반환
```

### 코드 2

```python
def solution(s):
    answer = True
    if len(s) != 4 and len(s) != 6: #문자열의 길이가 4 또는 6이 아닌경우
        return False # False를 반환
    s = list(s) # 문자열 하나하나 판단하기 위한 list 타입으로 변환
    for i in s:
        if i.isalpha(): # 문자열중 알파벳이 있는 경우 
            return False # False 반환
    return answer # 해당하는 조건이 없는 경우 미리 선언한 True가 반환된다
```

