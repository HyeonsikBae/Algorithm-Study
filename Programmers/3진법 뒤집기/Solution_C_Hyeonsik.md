## 3진법 뒤집기

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
int solution(int n) {
    int answer = 0;
    int *array;
    int i = 0, j = n;
    while (j > 0)
    {
        j /= 3;
        i++;
    }
    array = (int*)malloc(sizeof(int) * i);
    i = 0;
    while (n > 2)
    {
        array[i] = n % 3;
        n /= 3;
        i++;
    }
    array[i] = n;
    j = i;
    while (i >= 0)
    {
        answer += array[i] * pow(3, j-i);
        i--;
    }
    return answer;
}
```
