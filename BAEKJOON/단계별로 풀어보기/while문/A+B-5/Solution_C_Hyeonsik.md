## A+B-5

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int main(void)
{
	int a, b;
	while (1)
	{
		scanf("%d", &a);
		scanf("%d", &b);
		if (a == 0 && b == 0)
			return (0);
		printf("%d\n", a + b);
	}
}
```
