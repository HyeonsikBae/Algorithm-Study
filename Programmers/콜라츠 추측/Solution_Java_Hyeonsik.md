## 콜라츠 추측

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public int solution(int num) {
        long answer = (long)num;
        //overflow 방지하여 long 타입으로 캐스팅
        for (int i = 0;i < 500;i++)
            //500회 반복
        {
            if (answer == 1)
                //결과값이 1이 나오면
                return i;
            	//반복횟수 i 반환
            answer = (answer % 2 == 0) ? answer / 2 : answer * 3 + 1;
            //answer가 짝수면, answer = answer / 2
            //answer가 홀수면, answer = answer * 3 + 1
        }
        return -1;
        //반복횟수 500 초과하여 for문 내에서 반환이 없으면 -1 반환
    }
}
```
