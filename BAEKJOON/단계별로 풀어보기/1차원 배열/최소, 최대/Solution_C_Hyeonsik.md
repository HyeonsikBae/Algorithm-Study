## 최소, 최대

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int		main(void)
{
	int	cnt;
	int max = -1000000, min = 1000000;
	scanf("%d", &cnt);
	int array[cnt];
	for (int i = 0; i < cnt; i++)
	{
		scanf("%d", &array[i]);
		if (array[i] > max)
			max = array[i];
		if (array[i] < min)
			min = array[i];
	}
	printf("%d %d", min, max);
	return (0);
}
```
