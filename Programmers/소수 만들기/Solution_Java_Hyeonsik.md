## 소수 만들기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public int solution(int[] nums) {
        int answer = 0;
        //정수형 변수 answer 선언 및 초기값 0 대입.
        for (int i = 0;i < nums.length - 2;i++) {
            // 0번재 인덱스부터 마지막 -2 번째 인덱스까지 반복
            for (int j = i + 1;j < nums.length - 1;j++){
                // i 다음 인덱스부터 마지막 -1 번째 인덱스까지 반복
                for (int k = j + 1;k < nums.length; k++){
                    // j 다음 인덱스부터 마지막 인덱스까지 반복
                    if(check_prime(nums[i] + nums[j] + nums[k]))
                        // i, j, k 번째 인덱스 수의 합 소수 판별하여 소수이면, 
                        answer++;
                    	// answer 값 증가
                }
            }
        }
        return answer;
        // answer 반환
    }
    public boolean check_prime(int number) {
        boolean flag = true;
        // boolean 형 변수 flag 선언 및 초기값 true 대입
        for(int i = 2; i <= Math.sqrt(number); i++){
            // 2부터 number의 제곱근까지 반복
            if (number % i == 0){
                // number 가 i로 나누어떨어지면
                flag = false;
                // flag 에 false 대입
                break;
                // 반복문 탈출
            }
        }
        return flag;
        // flag 반환
    }
}
```
