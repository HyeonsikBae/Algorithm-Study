## 두 정수 사이의 합

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
    public long solution(int a, int b) {
        long answer = 0;
        for (int i = Math.min(a, b);i <= Math.max(a, b);i++)
            //정수형 변수 i를 a, b중 min값부터 max값까지 반복
            answer += i;
        	//answer 에 i 값 합산
        return answer;
    }
}
```



### 풀이

1. Math 클래스의 min 메소드를 통해 a, b 중 작은 값을 i 에 대입
2. answer 에 i 값 합산
3. Math 클래스의 max 메소드를 통해 a, b 중 큰 값까지 i 증가하며 반복
4. answer 값 반환
