## 정수 제곱근 판별

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public long solution(long n) {
        long answer = 0;
        long temp = (long)Math.sqrt(n);
        //정수형 변수 temp 에 정수형으로 캐스팅 된 n의 제곱근 값 대입.
        answer = (n == temp*temp) ? (long)Math.pow(temp + 1, 2) : -1;
        //temp의 제곱이 n과 같으면
        	//answer 값에 (temp+1)의 제곱 대입
        //temp의 제곱이 n과 같지 않으면
        	//answer 값에 -1 대입
        return answer;
    }
}
```



### 풀이

1. Math 클래스의 sqrt 메소드를 통해 n의 제곱근을 구하고 long 타입으로 캐스팅하여 temp에 대입
2. temp의 제곱이 n과 같으면, 
3. Math 클래스의 pow 메소드를 통해 (n+1)의 제곱을 answer에 대입
4. temp의 제곱이 n과 같지 않으면,
5. answer에 -1 대입.
6. answer 값 반환
