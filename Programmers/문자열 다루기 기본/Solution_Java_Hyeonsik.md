## 문자열 내림차순으로 배치하기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public boolean solution(String s) {
        boolean answer = true;
        //boolean형 변수 answer 선언 및 초기값 선언
        if(s.length() == 4 || s.length() == 6){
            //s의 길이가 4 or 6이면
            for(int i = 0;i < s.length();i++){
                //s의 길이만큼 반복
                if(s.charAt(i) < '0' || s.charAt(i) > '9'){
                    //s의 i번째 문자가 0 ~ 9 사이가 아니면
                    answer = false;
                    //answer에 false 대입
                    break;
                    //반복문 탈출
                }
            }
        }
        else
            //s의 길이가 4 or 6이 아니면
            answer = false;
        	//answer에 false 대입
        return answer;
        //answer 반환
    }
}
```
