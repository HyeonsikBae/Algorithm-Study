## 멀쩡한 사각형

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

int ft_gcd(int w, int h);

long long solution(int w, int h) {
    long long answer = (long long)w * (long long)h;
    int gcd = ft_gcd(w, h);
    int dummy = w / gcd + h / gcd - 1;
    answer -= dummy * gcd;
    return answer;
}

int ft_gcd(int w, int h)
{
    int rtn = 1;
    int result = rtn;
    int temp = (w > h ? h : w);
    while (rtn <= temp)
    {
        if (w % rtn == 0 && h % rtn == 0)
            result = rtn;
        rtn++;
    }
    return (result);
}
```
