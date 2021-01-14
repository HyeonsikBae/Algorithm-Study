## 시험 성적

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int main(void)
{
    int num;
    scanf("%d", &num);
    if (num >= 90)
        printf("A");
    else if (num >= 80)
        printf("B");
    else if (num >= 70)
        printf("C");
    else if (num >= 60)
        printf("D");
    else
        printf("F");
    return (0);
}
```
