## 이상한 문자 만들기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public String solution(String s) {
        String answer = "";
        char character = ' ';
        //임의의 char형 변수 선언
        int temp = 0;
        //임의의 int형 변수 선언
        for(int i = 0;i<s.length();i++)
            //s의 길이만큼 반복
        {
            if(s.charAt(i) == ' ')
                //s의 i번째 문자가 space이면
            {
                character = ' ';
                //character 는 space
                temp = 0;
                //temp 초기화
            }
            else 
            {
                if(temp % 2 == 0)
                    //temp가 짝수이면
                    character = Character.toUpperCase(s.charAt(i));
                	//character는 i번째 문자 대문자로 변경
                else
                    //temp가 홀수이면
                    character = Character.toLowerCase(s.charAt(i));
                	//character는 i번째 문자 소문자로 변경
                temp++;
                //temp 증가
            }
            answer += character;
            //answer에 character 값 추가
        }
        return answer;
        //answer 반환
    }
}
```
