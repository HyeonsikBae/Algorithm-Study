## 문자열 반복

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <string.h>

int			main(void)
{
	int		count;
	int		r;
	char	str[20];

	scanf("%d", &count);
	for (int i = 0; i < count; i++)
	{
		scanf("%d", &r);
		scanf("%s", str);
		for (int j = 0; j < strlen(str); j++)
		{
			for (int k = 0; k < r; k++)
				printf("%c", str[j]);
		}
		printf("\n");
	}
	return (0);
}
```
