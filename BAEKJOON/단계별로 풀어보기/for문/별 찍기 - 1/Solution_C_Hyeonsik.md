## 별 찍기 - 1

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
int main(void)
{
    int num;
    scanf("%d", &num);
    for(int i = 1; i <= num; i++)
    {
        for(int j = 0; j < i; j++)
            printf("*");
        printf("\n");
    }
    return (0);
}
```
