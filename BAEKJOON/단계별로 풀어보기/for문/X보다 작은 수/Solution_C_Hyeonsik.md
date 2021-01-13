## X보다 작은 수

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int     main(void)
{
    int count, num, temp;
    scanf("%d %d", &count, &num);
    for(int i = 0; i < count; i++)
    {
        scanf("%d", &temp);
        if (temp < num)
            printf("%d ", temp);
    }
  	return (0);
}
```
