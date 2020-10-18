## 쿼드압축 후 개수 세기

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

void    quad(int *answer, int **arr, int row, int col, int size);
int check_same_all(int *answer, int **arr, int row, int col, int size);

int* solution(int** arr, size_t arr_rows, size_t arr_cols)
{
    int* answer = (int*)malloc(sizeof(int) * 2);
    answer[0] = 0, answer[1] = 0;
    quad(answer, arr, 0, 0, arr_rows);
    return answer;
}

void    quad(int *answer, int **arr, int row, int col, int size)
{
    if (size == 1)
    {
        if (arr[row][col] == 1)
            answer[1] += 1;
        else
            answer[0] += 1;
        return ;
    }
    else
    {
        if (check_same_all(answer, arr, row, col, size) == 1)
            return ;
        else
        {
            quad(answer, arr, row, col, size / 2);
            quad(answer, arr, row, col + size / 2 , size / 2);
            quad(answer, arr, row + size / 2, col, size / 2);
            quad(answer, arr, row + size / 2, col + size / 2, size / 2);
        }
    }
}

int check_same_all(int *answer, int **arr, int row, int col, int size)
{
    for(int i = 0;i < size;i++)
    {
        for(int j = 0;j < size;j++)
        {
            if (arr[row + i][col + j] != arr[row][col])
                return (-1);
        }
    }
    if (arr[row][col] == 0)
        answer[0] += 1;
    else
        answer[1] += 1;
    return (1);
}
```
