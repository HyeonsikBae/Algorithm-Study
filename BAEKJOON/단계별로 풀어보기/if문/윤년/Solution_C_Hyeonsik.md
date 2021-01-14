## 윤년

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
int main(void)
{
    int num;
    scanf("%d", &num);
    if (num % 4 == 0)
    {
        if (num % 400 == 0)
            printf("1");
        else if (num % 100 == 0)
            printf("0");
        else
            printf("1");
    }
    else
        printf("0");
    return (0);
}
```
