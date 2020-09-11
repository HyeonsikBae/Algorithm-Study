## 수박수박수박수박수박수?

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public String solution(int n) {
        String answer = "";
        for(int i = 0;i<n;i++)
        //n 크기만큼 반복
        {
            if(i % 2 == 0)
                //i가 짝수이면
                answer += "수";
           		//answer에 "수" 합산
            else
                //i가 홀수이면
                answer += "박";
            	//answer에 "박" 합산
        }
        return answer;
        //answer 반환
    }
}
```
