## 하샤드 수

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public boolean solution(int x) {
        boolean answer = true;
        //boolean 변수 answer 선언 및 초기화
        String s = x + "";
        //String 변수 s에 x 합산
        int temp = x;
        //int 변수 temp 선언 및 x 대입
        int sum = 0;
        //int 변수 sum 선언 및 초기화
        for (int i = 0;i < s.length();i++){
            //s의 길이만큼 반복
            sum += temp % 10;
            //sum 에 temp % 10 합산
            temp /= 10;
            //temp = temp / 10
        }
        if (x % sum != 0)
            //x 를 sum으로 나눈 나머지가 0이 아니면
            answer = false;
        	//answer 에 false 대입
        return answer;
        //answer 반환
    }
}
```
