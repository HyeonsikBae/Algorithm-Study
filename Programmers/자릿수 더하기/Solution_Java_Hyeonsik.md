## 자릿수 더하기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
import java.util.*;

public class Solution {
    public int solution(int n) {
        return recursive(n);
        //recursive(n) 반환
    }
    public int recursive(int n) {
        int result = 0;
        //int형 변수 result 선언 및 0 대입
        if(n > 0)
            //n이 0보다 크면
            result += (n % 10 + recursive(n / 10));
        	//result에 n % 10 합산.
        	//result에 recursive(n / 10) 합산.
        	//재귀를 통하여 n의 각 자릿수 합산.
        return result;
        //result 반환
    }
}
```
