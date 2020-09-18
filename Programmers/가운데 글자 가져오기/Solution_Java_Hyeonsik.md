## 가운데 글자 가져오기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public String solution(String s) {
        String answer = "";
        //String형 변수 answer 선언 및 초기화
        int size = s.length();
        //int형 변수 size 선언 및 s의 길이 대입
        if(size % 2 == 0)
            //size가 짝수이면
            answer += s.charAt(size / 2 - 1);
        	//answer에 s의 (size / 2 - 1)번째 문자 합산
        answer += s.charAt(size/2);
        //answer에 s의 (size / 2)번째 문자 합산
        return answer;
        //answer 반환
    }
}
```
