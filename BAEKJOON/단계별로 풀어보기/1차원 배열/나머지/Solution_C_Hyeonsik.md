## 나머지

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int		main(void)
{
	int rtn = 0;
	int array[42] = {0};
	int num;
	for(int i = 0; i < 10; i++)
	{
		scanf("%d", &num);
		array[num % 42]++;
	}
	for(int i = 0; i < 42; i++)
		if (array[i] > 0) rtn++;
	printf("%d", rtn);
	return (0);
}
```
