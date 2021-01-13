## 합

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
int main(void)
{
    int n, sum = 0;
    scanf("%d", &n);
    for(n; n > 0; n--)
        sum += n;
    printf("%d", sum);
}
```
