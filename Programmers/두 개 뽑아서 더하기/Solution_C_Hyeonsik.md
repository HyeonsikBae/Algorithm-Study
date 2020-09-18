## 두 개 뽑아서 더하기

언어 : C

작성 : Hyeonsik Bae

### 코드

```java
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

long combination_size(int n, int r);
//조합의 수 구하는 함수
int remove_duplicate(int array[], long size);
//중복 제거 함수
void selection_sort(int array[], long n);
//선택 정렬 함수

int* solution(int numbers[], size_t numbers_len) {
    long size_max = combination_size(numbers_len, 2);
    //long 타입 size_max 선언 및 조합의 수 대입
    int* temp = (int*)malloc(sizeof(int) * size_max);
    //int형 포인터 temp 선언 및 size_max만큼의 메모리 동적 할당
    int count = 0;
    //int형 변수 count 선언 및 초기화
    for(int i = 0;i < numbers_len - 1;i++){
        //인덱스 0 ~ numbers_len - 1 까지 반복
        for(int j = i + 1;j < numbers_len;j++)
            //인덱스 i + 1 ~ numbers_len 까지 반복
            temp[count++] = numbers[i] + numbers[j];
        	//temp에 두 수의 합을 모두 대입
    }
    selection_sort(temp, size_max);
    //temp 정렬
    size_max = remove_duplicate(temp, size_max);
    //size_max에 중복제거한 사이즈 대입 및 temp 내 중복 제거
    int* answer = (int*)malloc(sizeof(int) * size_max);
    //int형 포인터 answer 선언 및 size_max만큼의 메모리 동적 할당
    for(long i = 0;i < size_max;i++)
        //size_max만큼 반복
        *(answer + i) = *(temp + i);
    	//temp 내 값을 answer에 대입
    return answer;
    //answer 반환
}
long combination_size(int n, int r){
    return (n * (n - 1) / r);
}
int remove_duplicate(int array[], long size){
    int new_size = 0;
    for(long i = 0;i < size - 1;i++){
        if(array[i] == array[i + 1]){
            for(long j = i;j < size - 1;j++){
                array[j] = array[j + 1];
                array[j + 1] = -1;
            }
            if(array[i] == array[i+1] && array[i+1] != -1)
                i--;
        }
    }
    for(long i = 0;i < size;i++){
        if(array[i] != -1)
            new_size++;
        else
            break;
    }
    return new_size;
}
void selection_sort(int array[], long n)
{
    int least, temp;
    for(long i = 0;i < (n - 1);i++)
    {
        least = i;
        for(long j = i + 1;j < n;j++)
        {
            if(array[least] > array[j])
                least = j;
        }
        temp = array[i];
        array[i] = array[least];
        array[least] = temp;
    }
}
```
