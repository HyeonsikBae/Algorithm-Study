## 두 수 비교하기

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int main(void)
{
    int num1, num2;
    scanf("%d %d", &num1, &num2);
    if (num1 > num2)
        printf(">");
    else if (num1 < num2)
        printf("<");
    else
        printf("==");
    return (0);
}
```
