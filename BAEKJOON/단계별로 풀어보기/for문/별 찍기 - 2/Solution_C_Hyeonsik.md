## 별 찍기 - 2

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int     main(void)
{
    int num;
    scanf("%d", &num);
    for(int i = 0; i < num; i++)
    {
        for(int j = 0; j < num - i - 1; j++)
            printf(" ");
        for(int j = 0; j < i + 1; j++)
            printf("*");
        printf("\n");
    }
    return (0);
}
```
