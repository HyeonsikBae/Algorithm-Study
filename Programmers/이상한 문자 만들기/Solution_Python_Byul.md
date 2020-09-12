## 이상한 문자 만들기

언어 : Python

작성 : Byul Han

### 코드

```python
def solution(s):
    list_s = list(s) # 반복문과 대소문자 변경을 위해 list 타입으로 바꿔줌
    answer = ''
    index = 0
    for word in list_s:
        if word == " ": # 공백이 오는 경우
            answer += word # 공백을 더해줌
            index = 0 # 홀짝을 판별하기 위한 index 초기화
            continue
        if index % 2 == 0:
            answer += word.upper() # 인덱스가 짝수인 경우 대문자 
        else:
            answer += word.lower() # 인덱스가 홀수인 경우 소문자
        index += 1 # 한칸씩 이동할 때마다 인덱스를 늘려줌
    return answer
```
