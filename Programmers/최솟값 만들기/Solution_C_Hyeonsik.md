## 최솟값 만들기

언어 : C

작성 : Hyeonsik Bae

### 코드 #1 > 효율성 테스트 fail

- A 배열의 최댓값, B 배열의 최솟값을 각각 구해 곱한 값을 더하는 방식

```c
int			array_max(int A[], int A_len)
{
	int		temp = -1;
	int		index = 0;
	for (int i = 0; i < A_len; i++)
	{
		if (A[i] > temp)
		{
			temp = A[i];
			index = i;
		}
	}
	A[index] = -1;
	return (temp);
}

int			array_min(int A[], int A_len)
{
	int		temp = 1001;
	int		index = 0;
	for (int i = 0; i < A_len; i++)
	{
		if (A[i] < temp)
		{
			temp = A[i];
			index = i;
		}
	}
	A[index] = 1001;
	return (temp);
}

int			solution(int A[], int A_len, int B[], int B_len)
{
	int		answer = 0;
	
	for (int i = 0; i < A_len; i++)
		answer += (array_max(A, A_len) * array_min(B, B_len));
	return (answer);
}
```

### 코드 #2 > 효율성 테스트 fail

- A 배열을 오름차순, B 배열을 내림차순으로 정렬한 뒤 각 index에 해당하는 값을 곱하여 더하는 방식
- bubble sort 사용

```c
void		sort_z_to_a(int arr[], int len)
{
	int		temp;
	
	for (int i = 0; i < len; i++)
	{
		for (int j = 0; j < len - 1; j++)
		{
			if (arr[j] < arr[j + 1])
			{
				temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
			}
		}
	}
}

void		sort_a_to_z(int arr[], int len)
{
	int		temp;
	
	for (int i = 0; i < len; i++)
	{
		for (int j = 0; j < len - 1; j++)
		{
			if (arr[j] > arr[j + 1])
			{
				temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
			}
		}
	}
}

int			solution(int A[], int A_len, int B[], int B_len)
{
	int		answer = 0;
  
	sort_a_to_z(A, A_len);
	sort_z_to_a(B, B_len);
	for (int i = 0; i < A_len; i++)
		answer += A[i] * B[i];
	return (answer);
}
```

### 코드 #3 > 통과

- A 배열을 오름차순, B 배열을 내림차순으로 정렬한 뒤 각 index에 해당하는 값을 곱하여 더하는 방식
- quick sort 사용

```c
int			compare_a_to_z(const void *a, const void *b)
{
	int 	num1 = *(int *)a;
	int 	num2 = *(int *)b;
	if (num1 < num2)
        return -1;
	if (num1 > num2)
        return 1;
    return 0;
}

int			compare_z_to_a(const void *a, const void *b)
{
	int 	num1 = *(int *)a;
	int 	num2 = *(int *)b;
	if (num1 > num2)
        return -1;
	if (num1 < num2)
        return 1;
    return 0;
}

int			solution(int A[], int A_len, int B[], int B_len)
{
	int		answer = 0;
	qsort(A, A_len, sizeof(int), compare_a_to_z);
	qsort(B, B_len, sizeof(int), compare_z_to_a);
	for (int i = 0; i < A_len; i++)
		answer += A[i] * B[i];
	return (answer);
}
```

