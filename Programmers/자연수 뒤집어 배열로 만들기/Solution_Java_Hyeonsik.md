## 자연수 뒤집어 배열로 만들기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
import java.util.*;

public class Solution
{
	public static int[] solution(long n) {
        String temp = n + "";
        //String 변수 temp에 long 대입
        int answer[] = new int[temp.length()];
        //temp의 길이만큼의 int형 배열 answer 선언
        for(int i = 0;i < temp.length();i++){
            //temp의 길이만큼 반복
            answer[i] = (int)(n % 10);
            //answer의 i번 인덱스에 n % 10 대입.
            n /= 10;
            //n = n / 10
        }
        return answer;
        //answer 반환
    }
}
```
