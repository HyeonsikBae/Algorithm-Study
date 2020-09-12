## 2016년

언어 : Python

작성 : Byul Han

### 코드

```Python
def solution(a, b):
    days = ["THU", "FRI", "SAT", "SUN", "MON", "TUE", "WED"] 
    # 요일을 배열에 선언, 1월 1일이 금요일이므로 index 0에 목요일부터 순차적으로 선언
    months = [31, 29, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
    # 1월부터 12월까지 각 달의 날짜 수를 배열에 선언
    check = sum(months[:a - 1]) + b
    # 원하는 달 이전까지 달까지 합산한 후 b값을 더해줌
    answer = days[check % 7]
    # 요일은 7일을 주기로 반복되기 때문에 7로 나눠서 days의 값을 answer에 넣어줌
    return answer
```

