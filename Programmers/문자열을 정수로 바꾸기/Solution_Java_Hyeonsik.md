## 문자열을 정수로 바꾸기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public int solution(String s) {
        int answer = 0;
        //int형 변수 answer 선언 및 초기화
        answer = Integer.parseInt(s);
        //answer에 s를 int형으로 변환하여 대입
        return answer;
        //answer 반환
    }
}
```
