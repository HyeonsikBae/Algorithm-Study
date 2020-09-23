## N개의 최소공배수

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public int solution(int[] arr) {
        int answer = arr[0];
        //int형 변수 answer 선언 및 arr[0] 값 대입
        for(int i = 1;i < arr.length;i++) {
            //arr 길이 -1 만큼 반복 (0번째 인덱스값은 미리 대입하였음.)
            answer = lcm(answer, arr[i]);
            //answer 에 기존 값과 i번째 인덱스값의 최소공배수 대입
            //answer의 기존 값은 초기값은 arr[0], 다음부턴 arr[i-1]까지의 최소공배수이다.
        }
        return answer;
        //answer 반환
    }
    
    //최대공약수 공식 (유클리드 호제법)
    public int gcd(int a, int b) {
        return (b != 0 ? gcd(b, a % b) : a);
    }
    
    //최소공배수 공식 (a * b / gcd)
    public int lcm(int a, int b) {
        return a * b / gcd(a, b);
    }
}
```
