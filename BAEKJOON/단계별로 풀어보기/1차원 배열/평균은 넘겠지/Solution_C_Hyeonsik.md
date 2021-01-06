## 평균은 넘겠지

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <stdlib.h>

int			main(void)
{
	int		caseCount, studentCount, overCount;
	double	avg;
	int		*score;
	scanf("%d", &caseCount);
	for (int i = 0; i < caseCount; i++)
	{
		avg = overCount = 0;
		scanf("%d", &studentCount);
		if (!(score = (int*)malloc(sizeof(int) * studentCount)))
			return (-1);
		for (int j = 0; j < studentCount; j++)
		{
			scanf("%d", &score[j]);
			avg += score[j];
		}
		avg /= (double)studentCount;
		for (int j = 0; j < studentCount; j++)
		{
			if (score[j] > avg)
				overCount++;
		}
		printf("%.3lf%%\n", (double)overCount / studentCount * 100);
	}
	free(score);
	return (0);
}
```
