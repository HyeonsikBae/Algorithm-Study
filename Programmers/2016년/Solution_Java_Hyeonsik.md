## 2016년

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public String solution(int a, int b) {
        String answer = "";
        String[] weekday = {"SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"};
        //요일을 담은 String형 배열 선언
        int temp = 4;
        //1월 1일이 THU인 것을 감안한 초기값 선언
        for(int i = 1;i < a;i++)
        //a값 이전까지 반복
        {
            if (i <= 7)
            //i가 7보다 같거나 작으면
            {
                if (i == 2)
                //i가 2이면
                    temp += 29;
                	//temp에 29 합산 (윤년 적용)
                else
                //i가 2가 아니고 7보다 같거나 작으면
                    temp += (i % 2 == 0) ? 30 : 31;
                	//i가 짝수이면 temp에 30, 홀수이면 temp에 31 합산
            }
            else
            //i가 7보다 크면
                temp += (i % 2 == 0) ? 31 : 30;
            	//i가 짝수이면 temp에 31, 홀수이면 temp에 30 합산
        }
        temp += b;
        //temp에 b합산
        answer = weekday[temp % 7];
        //answer에 weekday의 해당 요일값 대입
        return answer;
        //answer 반환
    }
}
```
