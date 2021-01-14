## 알람 시계

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
int main(void)
{
    int h, m;
    scanf("%d %d", &h, &m);
    m -= 45;
    if (m < 0)
    {
        m += 60;
        h -= 1;
        if (h < 0)
            h +=24;
    }
    printf("%d %d", h, m);
    return (0);
}
```
