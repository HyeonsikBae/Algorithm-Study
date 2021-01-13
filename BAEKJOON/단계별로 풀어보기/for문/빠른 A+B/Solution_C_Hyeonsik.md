## 빠른 A+B

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int     main(void)
{
    int count, num1, num2;
    scanf("%d", &count);
    for(int i = 0; i < count; i++)
    {
        scanf("%d %d", &num1, &num2);
        printf("%d\n", num1 + num2);
    }
    return (0);
}
```
