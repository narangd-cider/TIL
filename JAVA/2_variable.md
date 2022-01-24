>**[ 남궁성의 정석코딩/ 자바의 정석 기초편 강의 ] 및 [ Java의 정석 ] 교재 를 학습한 후 정리하였습니다.**

</br>

# 2. Variable
### 📌 변수와 상수

* **변수란?**

  * 하나의 값을 저장할 수 있는 메모리 공간
  <br/><br/>

* **변수의 선언과 초기화**

  * 변수의 선언을 통해 값을 저장할 공간을 마련
  * 지역변수는 사용되기 전에 반드시 초기화 진행
  * 클래스변수와 인스턴스변수는 초기화를 생략할 수 있음
  <br/><br/>

* **변수의 명명규칙**

  * 대소문자가 구분되며 길이에 제한이 없음
  * 예약어 사용 금지
  * 숫자로 시작 금지
  * 특수문자는 '_'와 '$'만 허용 가능
  <br/><br/>

###  📌 변수의 타입
* **기본형(primitive type)**

  * 문자형: char
  * 숫자형: 정수형(byte, short, int, long) / 실수형(float, double)
  * 논리형: boolean
  <br/><br/>

* **상수와 리터럴(constant & literal)**
  * 상수는 변수와 달리 한번 값을 저장하면 다른 값으로 변경 불가능
  * 리터럴은 그 자체로 값을 의미
  * 변수와 리터럴 타입이 불일치하는 경우 
    * 변수 < 리터럴: error
    * byte, short 변수는 별도의 리터럴 타입이 없기 때문에 int 리터럴 저장 가능
    <br/><br/>
    ```java
    // 리터럴의 접두사와 접미사
    int i = 100; // 10진수
    int oct = 0100; // 8진수
    int hex = 0x100 // 16진수
 
    long i = 10_000_000_000L; // L 생략 불가능
    long i = 100; 
    float f = 3.14f; // f 생략 불가능
    double d = 3.14d; // d 생략 가능
 
    // 변수 > 리터럴 
    int i = 'A' // int > char
    long i = 123; // long > int
    double d = 3.14f; // double > float
 
    // 변수 < 리터럴 에러 발생
    int i = 30_0000_0000 // int의 범위를 벗어남
    long i = 3.14f // long < float
    float f = 3.14; // float < double 
     ```
    <br/>

* **형식화된 출력 - printf( )**
  
  * println( ) 출력 형식 지정 불가능
  * printf( )로 출력 형식 지정 가능
  <br/><br/>
    ```java
    // println 출력형식 지정 불가
    System.out.println(10.0/3); // 3.3333333... (실수의 자리수 조절 불가)
    System.out.println(0x1A); // 26 (10진수로만 출력 가능)
    
    // printf 출력형식 지정 가능
    System.out.printf("%2f", 10.0/3); // 3.33
    System.out.printf("%d", 0x1A); // 26
    System.out.printf("%x", 0x1A); // 1A
    
    /* printf 지시자
    논리형 %b
    정수형 %d, %o, %x, %X
    실수형 %f, %e, %E
    문자형 %c, %s
    */
    
    // 정수를 10, 8, 16진수로 출력
    System.out.printf("%d",15); // 15
    System.out.printf("%o",15); // 17
    System.out.printf("%x", 15); // f
    System.out.printf("%s", integer.toBinaryString(15)); // 1111 (toBinaryString 정수>2진수 변환 메소드)
    
    // 8진수와 16진수에 접두사 붙이기
    System.out.printf("%#o",15); // 017
    System.out.printf("%#x",15); // 0xf
    System.out.printf("%#X", 15); // 0XE
    
    // 실수 출력을 위한 지시자 %f, 지수형식 %e, 간략한 형식 %g
    float f = 123.4567890
    System.out.printf("%f",f); // 123.456787 (소수점 아래 6자리)
    System.out.printf("%e",f); // 1.234568e+02
    System.out.printf("%g",123.456789); // 123.457 (소수점 포함 7자리)
    System.out.printf("%g",0.00000001); // 1.00000e-8
    
    System.out.printf("[%5d]%n", 10); // [   10] (앞에 세자리 공백)
    System.out.printf("[%-5d]%n", 10); // [10   ] (왼쪽 정렬, 뒤에 세자리 공백)
    System.out.printf("[%05d]%n", 10); // [00010] (공백을 0으로 채움. 값이 지정한 자리수보다 큰 경우 짤리지 않고 모두 출력)
    
    System.out.printf("d=%14.10f%n",d); // 전체 14자리 중 소수점 아래 10자리
    
    System.out.printf("[%s]%n", url);   // [www.codechobo.com]
    System.out.printf("[%20s]%n", url); // [   www.codechobo.com]
    System.out.printf("[%-20s]%n", url);// [www.codechobo.com   ] (왼쪽 정렬)
    System.out.printf("[%8s]%n", url)   // [www.code] (8자리만 출력)
    ```
  <br/>

* **화면에서 입력받기 - Scanner**
  * Scanner: 화면으로부터 데이터를 입력받는 기능을 제공하는 클래스
  <br/><br/>
    ```java
    //import문 추가
    import java.util.* 
    // 혹은 import java.util.Scanner
    
    // Scanner 객체 생성
    Scanner scanner = new Scanner(System.in)
    
    // Scanner 객체 사용
    int num01 = scanner.nextInt(); // 화면에서 입력받은 정수를 num에 저장
    int num02 = scanner.nextFloat();
    String input = scanner.nextLine() // 화면에서 입력받은 내용을 input에 저장
    int num03 = Integer.parseInt(input) // 문자열(inptu)을 숫자(num)으로 변환
    ```
  <br/>
 
### 📌 형변환

* **문자와 숫자간의 변환**
  * 3 + '0' → '3'
  * 3 + -'0' → '3' 
  <br/><br/>

* **문자열의 변환**
  * 3 + "" → "3"
  * '3' + "" → "3"
  <br/><br/>

* **문자열을 숫자로 변환**
  * "3" → (Integer.parseInt("3")) 3 
  * "3.4" → (Double.parseDouble("3.4") 3.4
  <br/><br/>
  
* **문자열을 문자로 변환**
  * "3" →(charAt(0)) '3' 