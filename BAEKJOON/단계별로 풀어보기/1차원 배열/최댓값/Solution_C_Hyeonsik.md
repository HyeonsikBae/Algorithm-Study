## 최댓값

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int		main(void)
{
	int	array[9];
	int max = 0, index;
	for(int i = 0; i < 9; i++)
	{
		scanf("%d", &array[i]);
		if (array[i] > max)
		{
			max = array[i];
			index = i;
		}
	}
	printf("%d\n%d", array[index], index + 1);
	return (0);
}
```
