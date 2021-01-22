## 알파벳 찾기

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <string.h>

int			main(void)
{
	char	str[100];
	int		index[26];
	scanf("%s", str);
	int		len = strlen(str);
	for(int i = 0; i < 26; i++)
		index[i] = -1;
	for(int i = 0; i < len; i++)
	{
		if (index[str[i] - '0' - 49] == -1)
			index[str[i] - '0' - 49] = i;
	}
	for(int i = 0; i < 26; i++)
		printf("%d ", index[i]);
	return (0);
}
```
