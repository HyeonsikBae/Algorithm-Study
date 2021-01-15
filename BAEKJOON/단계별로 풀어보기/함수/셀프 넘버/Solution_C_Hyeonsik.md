## 셀프 넘버

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int			ft_self_num(int num)
{
	int		sum = num;
	while (num > 0)
	{
		sum += num % 10;
		num /= 10;
	}
	return (sum);
}

int			main(void)
{
	int		array[10000];
	for (int i = 0; i < 10000; i++)
		array[i] = i + 1;
	for (int i = 0; i < 10000; i++)
	{
		if (ft_self_num(i + 1) < 10000)
			array[ft_self_num(i + 1) - 1] = 0;
	}
	for(int i = 0; i < 9999; i++)
	{
		if (array[i] != 0)
			printf("%d\n", array[i]);
	}
	return (0);
}
```
