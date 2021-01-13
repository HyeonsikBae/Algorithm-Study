## A+B-7

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
int main(void)
{
    int num1, num2, count;
    scanf("%d",&count);
    for(int i = 0; i < count; i++)
    {
        scanf("%d %d", &num1, &num2);
        printf("Case #%d: %d\n", i + 1, num1 + num2);
    }
    return (0);
}
```
