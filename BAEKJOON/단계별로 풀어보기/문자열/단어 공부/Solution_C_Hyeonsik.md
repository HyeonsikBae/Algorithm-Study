## 단어 공부

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int			main(void)
{
	char	string[1000000];
	scanf("%s", string);
	int		len = strlen(string);
	int		count[26] = {0, };
	int		max = 0, check = -1;
	for(int i = 0; i < len; i++)
	{
		if (islower(string[i]))
			string[i] = toupper(string[i]);
		count[string[i] - 'A']++;
	}
	for(int i = 0; i < 26; i++)
	{
		if (count[i] > max)
		{
			max = count[i];
			check = i;
		}
		else if (count[i] == max)
			check = -1;
	}
	check == -1 ? printf("?") : printf("%c", check + 'A');
	return (0);
}
```
