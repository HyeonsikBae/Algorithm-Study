## 더하기 사이클

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int main(void)
{
	int answer = 1;
	int array[3] = {0};
	int num;
	scanf ("%d", &num);
	array[0] = num / 10;
	array[1] = num % 10;
	while (1)
	{
		array[2] = (array[0] + array[1]) % 10;
		array[0] = array[1];
		array[1] = array[2];
		if (array[0] == num / 10 && array[1] == num % 10)
		{
			printf("%d", answer);
			break;
		}
		answer += 1;
	}
	return (0);
}
```
