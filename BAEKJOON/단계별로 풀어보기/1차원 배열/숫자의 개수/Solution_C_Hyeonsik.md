## 숫자의 개수

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int		main(void)
{
	int array[10] = {0};
	int	num = 1;
	int input;
	for(int i = 0; i < 3; i++)
	{
		scanf("%d", &input);
		num *= input;
	}
	while (num > 0)
	{
		array[num % 10] += 1;
		num /= 10;
	}
	for (int i = 0; i < 10; i++)
	{
		printf("%d\n", array[i]);
	}
	return (0);
}
```
