## 이진 변환 반복하기

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
int size_num(int n)
{
    int i = 1;
    
    while (n >= pow(2, i))
        i++;
    return i;
}

char *exchange_to_binary(int num)
{
    int i = size_num(num);
    char *rtn = (char*)malloc(sizeof(char) * (size_num(num) + 1));
    
    *(rtn + size_num(num)) = '\0';
    while (num > 0)
    {
        if (num % 2 == 1)
            *(rtn + i - 1) = '1';
        else
            *(rtn + i - 1) = '0';
        i -= 1;
        num /= 2;
    }
    return rtn;
}

int count_zero(char *s)
{
    int count = 0;
    int i = 0;
    while (*(s + i))
    {
        if (*(s + i) == '0')
            count++;
        i++;
    }
    return count;
}

int *solution(char const *str)
{
    char *s = (char*)malloc(sizeof(char) * (strlen(str) + 1));
    strcpy(s, str);
    int *answer = (int*)malloc(sizeof(int) * 2);
    answer[0] = 0;
    answer[1] = 0;
    
    while (!(s[0] == '1' && s[1] == '\0'))
    {
        answer[1] += count_zero(s);
        answer[0] += 1;
        s = exchange_to_binary(strlen(s) - count_zero(s));
    }
    return answer;
}
```
