## 올바른 괄호

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

// 파라미터로 주어지는 문자열은 const로 주어집니다. 변경하려면 문자열을 복사해서 사용하세요.
bool solution(const char* s) {
    bool answer = true;
    int count_open = 0, count_close = 0, count = 0;
    while (*(s + count))
    {
        if (*(s + count) == '(')
            count_open++;
        else
            count_close++;
        if (count_close > count_open)
        {
            answer = false;
            break ;
        }
        count++;
    }
    if (count_open != count_close)
        answer = false;
    return answer;
}
```
