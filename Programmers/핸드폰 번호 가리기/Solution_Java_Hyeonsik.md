## 핸드폰 번호 가리기

언어 : Java

작성 : Hyeonsik Bae

### 코드

```java
class Solution {
  public String solution(String phone_number) {
      String answer = "";
      //비어있는 String 타입 answer 선언
      int length = phone_number.length();
      //정수형 변수 length에 phone_number 의 길이 저장
      for(int i = 0;i < length-4;i++)
          //length 값 -4 만큼 반복
          answer += "*";
      	  //answer에 * 합산
      for(int i = 0;i < 4;i++)
          //4회 반복
          answer += phone_number.charAt(length - 4 + i);
      	  //answer에 phone_number의 마지막 -4 +i 자리의 값 합산
      return answer;
      //answer 반환
  }
}
```
