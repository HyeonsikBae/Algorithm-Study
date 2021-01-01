## 내적

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
int solution(int a[], size_t a_len, int b[], size_t b_len) {
    int answer = 0;
    int i = 0;
    while (i < a_len)
    {
        answer = answer + (a[i] * b[i]);
        i++;
    }
    return answer;
}
```

