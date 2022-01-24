>**`(남궁성의 정석코딩)자바의 정석 기초편 강의` 및 `Java의 정석 교재`를 학습한 후 정리하였습니다.**

</br>

# 4. 조건문과 반복문
### 📌 조건문 - if, switch

* **if문**

  * 조건식이 참일 때, 괄호안의 문장들을 수행
  * '0' <= ch && ch <= '9' 
    * 문자 ch가 숫자일 때
  * str.equals ("yes") 
    * 문자열 str의 내용이 "yes"일 때(대소문자 구분)
  * str.equalsIgnorecase("yES") 
    * 문자열 str의 내용이 "yes"일 때(대소문자 구분안함)
  <br/><br/>
 
* **if-else문**

  * 조건식이 참일 때와 거짓일 때로 나눠서 처리
  <br/><br/>

* **if-else if문**

  * 여러 개의 조건식을 포함한 조건식
  <br/><br/>

* **중첩 if문**

  * if문 안의 if(중첩횟수 제약 없음)
  <br/><br/>
    ```java
      switch(month) {
        case 3: case 4: case 5:
            System.out.println("현재 계절은 봄입니다.");
            // break문 삭제
        case 6: case 7: case 8:
            System.out.println("현재 계절은 여름입니다.");
            break;
        case 9: case 10: case 11:
            System.out.println("현재 계절은 가을입니다.");
            break;
        default:
        case 12: case 1: case 2:
            System.out.println("현재 계절은 겨울입니다.");
    
    // month가 3인 경우
    // 현재 계절은 봄입니다.
    // 현재 계절은 여름입니다. 두 문장 모두 출력됨(break;문이 없기 때문)  
    ```
 <br/>
 
* **switch문**

  * 처리해야 하는 경우의 수가 많을 때 유용한 조건문
  * 항상 if문으로 변환 가능
  * 조건식 결과는 정수 또는 문자열이어야 함
  * case문의 값은 정수 상수(문자 포함), 문자열만 가능, 중복되지 않아야 함
  <br/><br/>

### 📌 반복문 - for, while, do-while
* **for문**

  * 조건을 만족하는 동안 블럭 반복 → 반복횟수를 알 때 적합
  * for문 내에 또 다른 for문 포함 가능(중첩 for문)
  <br/><br/>
    ```java
    for(int i=1, j=10, i<=10;, i++, j--){ 
        System.out.println("i=" + i + ", j" + j);
    }
    // 조건문에 2개의 변수 사용 가능(단, 타입이 같아야 함)
    
    System.out.prinln(i); // 오류 발생
    // 조건문에 사용된 변수는 블럭 내부에서만 사용 가능
    // 블럭 외부에서 사용하려면 for문 밖에서 변수 선언
    // 변수 범위(scope): 선언 위치부터 선언된 블럭의 끝까지 유효
    
    for(;;) // 무한반복문
    ```
  <br/>

* **while문**

  * 조건을 만족하는 동안 블럭 반복 → 반복횟수 모를 때
  * if와 while문은 항상 서로 변환 가능
  * while(true) // 무한반복문, true 생략 불가
  <br/><br/>

* **do-while문**

  * 블럭을 최소한 한 번 이상 반복 → 사용자 입력 받을 때 유용 
  * if와 while문은 항상 서로 변환 가능
  <br/><br/>
 
* **break문**

  * 자신이 포함된 하나의 반복문을 벗어남
  <br/><br/>
 
* **continue문**

  * 자신이 포함된 반복문의 끝으로 이동 - 다음 반복으로 넘어감
  * 전체 반복 중에서 특정 조건시 반복을 건너뛸 때 유용함
  <br/><br/> 

* **이름 붙은 반복문**
  * 반복문에 이름을 붙여서 하나 이상의 반복문을 벗어날 수 있음