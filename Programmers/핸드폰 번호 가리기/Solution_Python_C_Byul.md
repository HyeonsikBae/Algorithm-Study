## 핸드폰 번호 가리기

언어 : Python, C

작성 : Byul Han

### C 코드

```C
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

char* solution(const char* phone_number) {
    int j = 0;
    int length = strlen(phone_number); // length 주어진 문자열의 길이 
    char* answer = (char*)malloc(sizeof(char)*(length + 1)); 
    // Null 까지 lenght + 1 크기를 할당 
    while (j < length - 4) // 마지막 4자리를 제외하고 '*' 채우기
    {
        answer[j] = '*';
        j++;
    }
    while (j <= length) // 남은 4자리는 받은 문자열의 4자리 가져오기
    {
        answer[j] = phone_number[j];
        j++;
    }
    answer[j] = '\0'
    return answer;
}
```

### Python 코드

```python
def solution(s):
    length = len(s) # 문자열의 길이
    s = s.replace(s[:length - 4], "*" * (length - 4))
    # 뒤에 네자리를 제외한 부분을 그 길이만큼 "*" 문자로 대치해준다
    return s
```

