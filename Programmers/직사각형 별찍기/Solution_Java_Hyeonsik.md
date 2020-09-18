## 직사각형 별찍기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        //Scanner method 선언
        String answer = "";
        //String형 변수 answer 선언 및 초기화
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        //int a, b를 표준 입력으로 받음.
        for(int i=0;i<b;i++)
        //b만큼 반복
        {
            for(int j=0;j<a;j++)
            //a만큼 반복
            {
                answer += "*";
                //answer에 "*" 합산
            }
            answer += "\n";
            //answer에 개행 합산
        }
        System.out.println(answer);
        //answer 출력
    }
}
```



### 풀이

1. Math 클래스의 sqrt 메소드를 통해 n의 제곱근을 구하고 long 타입으로 캐스팅하여 temp에 대입
2. temp의 제곱이 n과 같으면, 
3. Math 클래스의 pow 메소드를 통해 (n+1)의 제곱을 answer에 대입
4. temp의 제곱이 n과 같지 않으면,
5. answer에 -1 대입.
6. answer 값 반환
