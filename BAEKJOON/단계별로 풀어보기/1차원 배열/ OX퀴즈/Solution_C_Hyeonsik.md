## OX퀴즈

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <string.h>

int			main(void)
{
	int		cnt, i, j, score, answer;
	char	str[81];
	scanf("%d", &cnt);
	i = 0;
	while (i < cnt)
	{
		scanf("%s", str);
		str[strlen(str)] = '\0';
		j = answer = 0;
		score = 1;
		while (str[j])
		{
			if (str[j] == 'O')
			{
				answer += score;
				score++;
			}
			else
				score = 1;
			j++;
		}
		printf("%d\n", answer);
		i++;
	}
	return (0);
}
```
