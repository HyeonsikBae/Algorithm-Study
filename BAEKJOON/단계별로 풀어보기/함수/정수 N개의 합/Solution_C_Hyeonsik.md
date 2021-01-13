## 정수 N개의 합

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

long long sum(int *a, int n)
{
    long long	sum = 0;
    
    for(int i = 0;i < n;i++)
        sum += *(a + i);
    return (sum);
}
```
