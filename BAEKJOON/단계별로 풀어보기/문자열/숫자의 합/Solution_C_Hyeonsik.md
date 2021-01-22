## 숫자의 합

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int			main(void)
{
	int		count;
	scanf("%d", &count);
	char	string[count + 1];
	scanf("%s", string);
	int		sum = 0;
	for (int i = 0; i < count; i++)
		sum += string[i] - '0';
	printf("%d", sum);
	return (0);
}
```
