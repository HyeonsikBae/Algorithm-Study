## 스킬트리

언어 : C

작성 : Hyeonsik Bae

### 코드

```c
//const char * type을 char * type 으로 return
char    *ft_copy(const char *s2)
{
    char *s1;
    if (!(s1 = (char*)malloc(sizeof(char) * (strlen(s2) + 1))))
        return (NULL);
    int i = 0;
    while (*(s2 + i))
    {
        *(s1 + i) = *(s2 + i);
        i++;
    }
    *(s1 + i) = '\0';
    return (s1);
}

//skill을 배울 순서와 skill_tree를 비교
int     ft_check(char *sequence, char *skill)
{
    int i = 0;
    while (*(skill + i))
    {
        if (*(skill + i) == *(sequence + i))
            i++;
        else
            return (0);
    }
    return (1);
}

//skill tree에서 sequence에 해당하는 부분만 추출
int     ft_extract_sequence(char *sequence, char *skill)
{
    int len = strlen(sequence);
    char *result;
    if (!(result = (char*)malloc(sizeof(char) * (len + 1))))
        return (0);
    int i = 0,  j = 0, k = 0;
    while (*(skill + i))
    {
        j = 0;
        while (*(sequence + j))
        {
            if (*(sequence + j) == *(skill + i))
            {
                result[k] = *(skill + i);
                k++;
                break ;
            }
            j++;
        }
        i++;
    }
    result[k] = '\0';
    return (ft_check(sequence, result));
}

//solution
int solution(const char* skill, const char* skill_trees[], size_t skill_trees_len) {
    int answer = 0;
    int i = 0;
    char *sequence = ft_copy(skill);
    while (i < skill_trees_len)
    {
        char *test = ft_copy(skill_trees[i]);
        answer += ft_extract_sequence(sequence, test);
        free(test);
        i++;
    }
    free(sequence);
    return (answer);
}
```
