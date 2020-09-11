## 약수의 합

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
  public int solution(int n) {
      int answer = 0;
      for(int i = 1;i <= n / 2;i++)
          //n의 절반까지 반뽁
      {
          if (n % i == 0)
              //i가 n의 약수이면
              answer += i;
          //answer에 i 합산
      }
      return answer + n;
      //answer에 n 더한 값 반환
  }
}
```
