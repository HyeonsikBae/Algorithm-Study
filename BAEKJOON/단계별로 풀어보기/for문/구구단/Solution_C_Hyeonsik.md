## 구구단

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int main()
{
    int num;
    scanf("%d",&num);
    
    for(int i=0; i < 9; i++)
        printf("%d * %d = %d\n", num, i + 1, num * (i + 1));
    return (0);
}
```
