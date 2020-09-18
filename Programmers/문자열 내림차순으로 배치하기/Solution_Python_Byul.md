## 문자열 내림차순으로 배치하기

언어 : Python

작성 : Byul Han

### 코드

```python
def solution(s):
    sort_s = sorted(list(s)) # 문자열을 리스트형식으로 바꿔서 오름차순 정렬
    answer = '' # 답이 들어갈 문자형 변수 선언
    for i in sort_s:
        answer = i + answer # 문자열을 역순으로 answer에 넣어줌
    return answer
```

