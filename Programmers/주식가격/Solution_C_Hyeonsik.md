## 주식가격

언어 : C

작성 : Hyeonsik Bae

### 코드

```C
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>
#include <string.h>

int* solution(int prices[], size_t prices_len)
{
    int i, j, time;
    int* answer = (int*)malloc(sizeof(int)*prices_len);

    i = 0;
    while (i < prices_len - 1)
    {
        j = i + 1;
        time = 1;
        while (j < prices_len)
        {
            if (prices[i] > prices[j])
                break ;
            if (j == prices_len - 1)
                break;
            time++;
            j++;
        }
        answer[i] = time;
        i++;
    }
    answer[i] = 0;
    return answer;
}
```
