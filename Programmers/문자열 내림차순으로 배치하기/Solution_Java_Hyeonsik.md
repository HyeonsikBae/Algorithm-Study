## 문자열 내림차순으로 배치하기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
import java.util.*;
class Solution {
    public String solution(String s) {
        String answer = "";
        //정답을 담을 String형 변수 선언 및 초기화
        String[] list = s.split("");
        //String s를 ""로 split하여 담을 String형 배열 list 선언
        Arrays.sort(list, Collections.reverseOrder());
        //list 역순으로 정렬
        for(String str : list){
            //list 배열 값만큼 반복
            answer += str;
            //answer에 list의 배열을 순차적으로 합산
        }
        return answer;
        //answer 반환
    }
}
```
