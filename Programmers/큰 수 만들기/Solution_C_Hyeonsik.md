## 큰 수 만들기

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

char* solution(const char* number, int k) {
    int reslen = strlen(number) - k;
    int max;
    int ptr = 0;
    int j = 0;
    char* answer = (char*)malloc(sizeof(char) * (reslen + 1));
    answer[reslen] = '\0';
    while (k > 0 && j < reslen)
    {
        max = 0;
        for(int i = 0;i < k + 1;i++)
        {
            if (max < *(number + i + ptr) - '0')
                max = *(number + i + ptr) -'0';
        }
        for(int i = 0;i < k + 1;i++)
        {
            if (max == *(number + i + ptr) - '0')
            {
                ptr += i;
                k -= i;
                break;
            }
        }
        *(answer + j++) = *(number + ptr++);
    }
    while(j < reslen)
        *(answer + j++) = *(number + ptr++);
    return answer;
}
```
