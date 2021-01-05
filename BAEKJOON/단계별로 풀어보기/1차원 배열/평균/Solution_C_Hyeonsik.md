## 평균

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>

int		main(void)
{
	int cnt_subject;
	double max = 0, total = 0;
	scanf("%d", &cnt_subject);
	double array[cnt_subject];
	for (int i = 0; i < cnt_subject; i++)
	{
		scanf("%lf", &array[i]);
		if (array[i] > max)
			max = array[i];
	}
	for (int i = 0; i < cnt_subject; i++)
	{
		array[i] *= (100 / max);
		total += array[i];
	}
	printf("%.2lf", total / cnt_subject);
	return (0);
}
```
