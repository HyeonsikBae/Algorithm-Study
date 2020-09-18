## 평균 구하기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public double solution(int[] arr) {
        double answer = 0;
        //double 변수 answer 선언 및 초기화
        for(int i = 0;i < arr.length;i++){
            //arr의 길이만큼 반복
            answer += arr[i];
            //answer에 arr의 i번째 인덱스 값 합산
        }
        return answer / arr.length;
        //(answer / arr의 길이) 반환
    }
}
```
