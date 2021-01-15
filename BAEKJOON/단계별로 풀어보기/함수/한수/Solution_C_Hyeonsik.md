## 한수

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int			ft_check(int num)
{
	int	count = 0;
	int temp = num;
	while (temp > 0)
	{
		temp /= 10;
		count++;
	}
	int array[count];
	count = 0;
	while (num > 0)
	{
		array[count] = num % 10;
		count++;
		num /= 10;
	}
	while (count > 2)
	{
		if (array[count - 1] - array[count - 2] != array[count - 2] - array[count - 3])
			return (0);
		count--;
	}
	return (1);
}

int			main(void)
{
	int		num, sum = 0;
	scanf("%d", &num);
	while (num > 0)
	{
		sum += ft_check(num);
		num--;
	}
	printf("%d", sum);
	return (0);
}
```
