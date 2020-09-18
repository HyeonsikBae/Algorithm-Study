## 삼각 달팽이

언어 : C

작성 : Hyeonsik Bae

### 코드

```java
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

int* solution(int n) {
    // return 값은 malloc 등 동적 할당을 사용해주세요. 할당 길이는 상황에 맞게 변경해주세요.
    int* answer = (int*)calloc(n * (n+1) / 2, sizeof(int));
    //int형 변수 answer 선언 및 n * (n + 1) / 2 만큼 메모리 할당
    int temp[n][n];
    //n x n 크기의 int형 배열 temp 선언
    int re = n;
    //int형 변수 re 선언 및 n 대입. (반복 횟수)
    int col = 0, row = -1;
    //int형 변수 col, row 선언 및 초기화
    int a = 0, b = 0, c = 0, num = 0;
    //int형 변수 a, b, c, num 선언 및 초기화
    /*
    re : 방향 변경할 횟수를 정하는 변수
    col : 열
    row : 행
    a : re 만큼 반복하기 위한 변수
    b : 각 방향별 숫자를 몇 번 대입할지 정하는 변수
    c : 방향 변환 플래그
    num : 대입할 값
    */
    for(a = 0;a < re;a++){
        //re만큼 반복
        b = re - a;
        //해당 루틴에서 값을 몇 번 넣을지 대입
        if(c % 3 == 0){
            //c가 3의 배수이면
            while (b-- > 0)
                //b만큼 반복
                temp[++row][col] = ++num;
            	//행을 늘려가며 num 대입
        }
        else if(c % 3 == 1){
            //c가 3의 배수 + 1 이면
            while (b-- > 0)
                //b만큼 반복
                 temp[row][++col] = ++num;
            	//열을 늘려가며 num 대입
        }
        else{
            //c가 3의 배수 + 2 이면
            while (b-- > 0)
                //b만큼 반복
                temp[--row][--col] = ++num;
            	//행과 열을 줄여가며 num 대입
        }
        c++;
        //플래그 증가
    }
    int count = 0;
    //int형 변수 count 선언 및 초기화
    for(int i = 0;i < n;i++){
        //n만큼 반복 (temp배열 행)
        for(int j = 0;j <= i;j++)
            //i만큼 반복 (temp 열)
            answer[count++] = temp[i][j];
        	//answer 배열에 temp값을 대입
    }
    return answer;
    //answer 반환
}
```
