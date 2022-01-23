>**본 게시물은 남궁성의 정석코딩 자바의 정석 기초편 강의 및 Java의 정석 교재를 학습한 후 정리하였습니다.**

</br>

# 6. Object Oriented Programming Ⅰ
### 📌 객체지향언어

* **객체지향언어의 역사**
  
  * 80년 초 소프트웨어 위기 - 빠른 변화를 못쫓아감
  * 해결책으로 객체지향 언어 도입(절차적 > 객체지향)
  <br/><br/>

* **객체지향언어**
  
  * 코드의 재사용성이 높고, 유지보수가 용이, 중복 코드 제거
  * 객체지향 언어 = 프로그래밍 언어 + 객체지향 개념(규칙)
  * 핵심개념: 캡슐화, 상속, 추상화, 다형성
  <br/><br/>

### 📌 클래스와 객체
* **클래스와 객체의 정의와 용도**

  * 클래스의 정의: 객체를 정의해 놓은 것 / 설계도
  * 클래스의 용도: 객체를 생성하는데 사용
  * 객체의 정의: 실제로 존재하는 것. 사물 또는 개념 / 제품
  * 객체의 용도: 객체가 가지고 있는 기능과 속성에 따라 다름 
  <br/><br/>
 
* **객체와 인스턴스**

  * 객체 = 속성(변수) + 기능(메소드)
  * 객체: 모든 인스턴스를 대표하는 일반적 용어
  * 인스턴스: 특정 클래스로부터 생성된 객체
  <br/><br/>

* **객체의 구성요소 - 속성과 기능**

  * 클래스가 왜 필요한가? 객체를 생성하기 위해
  * 객체가 왜 필요한가? 객체를 사용하기 위해
  * 객체를 사용한다는 것은? 객체가 가진 속성과 기능을 사용하려고
  <br/><br/>

* **하나의 소스파일에 여러 클래스 작성**

  * public class가 있는 경우, 소스파일의 이름은 반드시 public class의 이름과 일치
    (대소문자까지 일치해야 함)
  * public class가 하나도 없는 경우(public을 붙이지 않은 class만 2개), 소스파일의 이름은 둘다 가능
  * 하나의 소스파일에 둘 이상의 public class가 존재하면 안 됨. 
  * 각 클래스를 별도의 소스파일에 나눠서 저장하던가 아니면 둘 중의 한 클래스에 public을 붙이지 않아야 함.
  <br/><br/>

* **인스턴스의 생성과 사용**
  * 객체의 생성
  <br/><br/>
    ```java
    /*
    클래스명 변수명; // 클래스의 객체를 참조하기 위한 참조변수 선언
    변수명 = new 클래스명( ); // 클래스의 객체를 생성 후, 객체의 주소를 참조변수에 저장
    클래스명 변수명 = new 클래스명( )
    */
    ```
  <br/>

  * 객체의 사용
  <br/><br/>
    ```java
    /*
    t.channel = 7; // Tv인스턴스의 멤버변수 channel의 값을 7로 한다.
    t.channelDown(); // Tv인스턴스의 메서드 channelDown()을 호출한다.
    System.out.println("현재 채널은 " + t.channel + " 입니다.");
    */
    ```
 <br/>

* **객체 배열**

  * 객체 배열 == 참조변수 배열
 <br/><br/>

* **클래스의 또 다른 정의**

  * 클래스 == 데이터 + 함수
  * 변수: 하나의 데이터를 저장할 수 있는 공간
  * 배열: 같은 종류의 여러 데이터를 하나로 저장할 수 있는 공간
  * 구조체: 서로 관련된 여러 데이터(종류 관계X)를 하나로 저장할 수 있는 공간
  * 클래스: 데이터와 함수의 결합(구조체 + 함수)
  * 클래스 ==  사용자 정의 타입
  <br/><br/>

### 📌변수와 메서드
* **선언위치에 따른 변수의 종류**

  * 클래스 변수: 클래스 영역, 클래스가 메모리에 올라갈 때 생성
  * 인스턴스 변수: 클래스 영역, 인스턴스가 생성되었을 때 생성
  * 지역변수: 클래스 영역 외(메서드 생성자, 초기화 블럭 내부), 변수 선언문이 수행되었을 때 생성
  <br/><br/>
    ```java
    class Variables // 클래스 영역(클래스 시작~끝): 변수, 메소드 선언문만 가능(순서는 상관없음. 일반적으로 변수 선언부터)
    {
        int iv;    // 인스턴스 변수(instance variable)
        static int cv; // 클래스 변수(static변수, 공유변수)
    
        void method() // 메소드 영역(메소드 시작~끝)
        {
            int lv = 0; // 지역변수(local variable)
        }
    }
    ```
  <br/>

* **클래스 변수와 인스턴스 변수**

  * 인스턴스 변수(개별 속성)
  * 클래스 변수(공통 속성)
  <br/><br/>
    ```java
    class Variables // 클래스 영역(클래스 시작~끝): 변수, 메소드 선언문만 가능(순서는 상관없음. 일반적으로 변수 선언부터)
    {
        int iv;    // 인스턴스 변수(instance variable)
        static int cv; // 클래스 변수(static변수, 공유변수)
    
        void method() // 메소드 영역(메소드 시작~끝)
        {
            int lv = 0; // 지역변수(local variable)
        }
    }
    
    Card c = new Card();
    c.kind = "HEART"
    c.number = 5;
    
    c.width = 200; 
    c.height = 300; // 가능하나 권장하지 않음
    
    Card.width = 200;
    Card.height = 300; // 권장(클래스명 기재)
    ```
  <br/>
 
* **메서드**

  * 문장들을 묶어놓은 것 / 반복적으로 수행되는 여러 문장을 메서드로 작성
  * 하나의 메서드는 한 가지 기능만 수행하도록 작성
  * 값(입력)을 받아서 처리하고, 결과를 반환(출력)
  * 장점: 중복코드 제거, 관리 용이, 재사용 가능
  * 지역변수(lv): 메서드 내에 선언된 변수(서로 다른 메서드 영역에 있는 변수명은 중복 가능)
  <br/><br/>
    ```java
    int add(int a, int b) // 선언부
    : 반환타입 메소드이름 (타입 변수명, 타입 변수명, ... )
    {    
        int result = a+b; // 메서드 호출시 수행될 코드
        return result; // 호출한 메소드로 결과 반환
    }    // 구현부
    ```
  <br/>

* **메서드의 선언과 구현**
  * 메서드이름(값1, 값2, ...); // 메서드를 호출하는 방법
  * 메서드는 클래스 영역에만 정의 가능
  <br/><br/>
    ```java
    MyMath mm = new MyMath(); // 먼저 인스턴스를 생성
    
    long value = mm.add(1L, 2L); // 메소드 호출
    
    long add(long a, long b) {
        long result = a+b;
        return result;
    }
    
    // main메서드에서 메서드 add 호출. 인수 1L와 2L가 메서드 add의 매개변수 a, b에 각각 복사(대입)
    // 메서드 add의 괄호{}안에 있는 문장들이 순서대로 수행
    // 메서드 add의 모든 문장이 실행되거나 return문을 만나면, 호출한 메서드(main메서드)로 되돌아와서 이후의 문장들을 실행
    ```

* **return문**

  * 실행 중인 메서드를 종료하고 호출한 곳으로 되돌아감
  * 반환 타입이 void인 경우 생략 가능(컴파일러가 자동 추가)
  * 반환 타입이 void가 아닌 경우 반드시 return문이 필요
  * 조건문의 경우 조건식이 참, 거짓일 때 모두 return문 필요
  <br/><br/>
 
* **호출 스택(call stack)**

  * 스택(stack): 밑이 막힌 상자. 위에 차곡차곡 쌓임
  * 메서드 수행에 필요한 메모리가 제공되는 공간
  * 메서드가 호출되면 호출스택에 메모리 할당. 종료되면 해제
  * 아래 있는 메서드가 위의 메서드를 호출한 것
  * 맨 위의 메서드 하나만 실행 중, 나머지는 대기 중
  <br/><br/>
 

* **기본형 매개변수와 참조형 매개변수**

  * 기본형 매개변수 - 변수의 값을 읽기만 할 수 있음(read only)
  * 참조형 매개변수 - 변수의 값을 읽고 변경할 수 있음(read & write)
  <br/><br/>

* **static 메서드와 인스턴스 메서드**

  * 인스턴스 메서드
    * 인스턴스 생성 후 '참조변수.메서드이름()'으로 호출
    * 인스턴스 멤버(iv, im)와 관련된 작업을 하는 메서드
    * 메서드 내에서 인스턴스 변수(iv) 사용가능
  * static 메서드(클래스 메서드)
    * 객체 생성없이 '클래스이름.메서드이름()'으로 호출
    * 인스턴스 멤버(iv, im)와 관련없는 작업을 하는 메서드
    * 메서드 내에서 인스턴스 변수(iv) 사용 불가
  * static을 언제 붙여야 할까?
    * 속성(멤버 변수) 중에서 공통 속성에 static을 붙임
    * 인스턴스 멤버(iv, im)을 사용하지 않는 메서드에 static을 붙임
  <br/><br/>

* **클래스 멤버와 인스턴스 멤버간의 참조와 호출**
  * static 메서드는 인스턴스 변수(iv)를 사용할 수 없음
  * static 메서드는 인스턴스 메서드(im)를 호출할 수 없음
  * static 메서드는 static메서드 호출 가능
  * 그러나 인스턴수 변수 사용 및 인스턴스 메서드 호출 불가
  * static 메서드 호출 시 객체(iv묶음)가 없을 수도 있어서 인스턴스 멤버 사용 불가능
  <br/><br/>

### 📌 오버로딩(overloading)
* **오버로딩이란?**

  * 한 클래스 안에 같은 이름의 메서드를 여러 개 정의하는 것
  <br/><br/>

* **오버로딩의 조건**

  * 메서드 이름이 같아야 함
  * 매개변수의 개수 또는 타입이 달라야 함
  * 반환 타입은 영향 없음
  <br/><br/>
    ```java
    // 오버로딩 X 
    int add(int a, int b) {return a+b;}
    int add(int x, int y) {return x+y;}
    
    int add(int a, int b) {return a+b;}
    long add(int a, int b) {return (long)a+b;}
    
    // 오버로딩 O - 그러나 ex) add(3, 3)인 경우 에러 발생(ambiguous)
    long add(int a, long b) {return a+b;}
    long add(long a, int b) {return a+b;}
    ```
  <br/>

* **(메서드) 오버로딩의 예**

  * 매개변수는 다르지만 같은 의미의 기능 수행
  <br/><br/>
 

### 📌 생성자(constructor)
* **생성자란? = iv 초기화 메서드**

  * 인스턴스가 생성될 때마다 호출되는 '인스턴스 초기화 메서드'
  * 인스턴스 생성시 수행할 작업(iv 초기화)에 사용
  <br/><br/>
    ```java
    Time t = new Time();
    t.hour = 12;
    t.minute = 34;
    t.second = 56;
    
    Timte t new TIme(12, 34, 56);
    ```
  <br/>
  
  * 이름이 클래스 이름과 같아야 함.
  * 리턴값이 없음(void 안붙임)
  * 모든 클래스는 반드시 생성자를 가져야 함
  <br/><br/>
    ```java
    class Card{
      Card () {    // 매개변수가 없는 생성자
         // 인스턴스 초기화 작업
      }
 
      Card(String kind, int number){    // 매개변수가 있는 생성자
          // 인스턴스 
      }
    } 
    ```
    <br/>
 
* **기본 생성자(default constructor)**

  * 매개변수가 없는 생성자
  * 생성자가 하나도 없을 때만, 컴파일러가 기본 생성자 자동 추가
  <br/><br/>
    ```java
    Class car {
        String color;
        String gearType;
        int door;
    
        Car() {} // 기본 생성자
        Car(String c, String g, int d) { // 매개변수가 있는 생성자
            color = c;
            gearType = g
            door. d;
        }
    }
    ```
    <br/>
  
* **생성자 this( )**

  * 생성자에서 다른 생성자 호출할 때 사용
  * 다른 생성자 호출 시 첫 줄에서만 사용 가능
  <br/><br/>
 
* **참조변수 this**
  * 인스턴스 자신을 가리키는 참조변수
  * 인스턴스 메서드(생성자 포함)에서 사용 가능
  * 지역변수(lv)와 인스턴스 변수(iv)를 구별할 때 사용
  * 인스턴스의 주소가 저장되어 있음
  * 모든 인스턴스 메서드에 지역변수로 숨겨진 채 존재
  <br/><br/>
    ```java
    class Car2{
      String color;
      String gearType;
      int door;
  
      Car2() {
          this("white", "auto", 4); // Car2(String color, String gearType, int door) 호출 - 중복 제거
      }
  
      Car2(String color) {
          this(color, "auto", 4);    // Car2(String color, String gearType, int door) 호출 - 중복 제거
      }
  
      Car2(String color, String gearType, int door) {
          this.color = color;
          this.gearType = gearType;
          this.door = door;
      }
  
    }
    ```
  <br/>
 
### 📌 변수의 초기화
* **변수의 초기화**

  * 지역변수(lv)는 사용 전 수동 초기화 필수
  * 멤버변수(iv, cv)는 0으로 자동 초기화
  <br/><br/>

* **명시적 초기화**

  * 대입연산자 = 사용
  <br/><br/>

* **초기화 블럭**

  * 인스턴스 초기화 블럭: { }   
  * 클래스 초기화 블럭: static { }
  <br/><br/>
    ```java
    // 멤버변수(iv, cv)의 초기화
    // 1. 자동 초기화
    
    // 2. 간단 초기화 - 명시적 초기화(=)
    class Car{
        int door = 4; // 기본형(primitive type) 변수의 초기화
        Engine e = new Engine(); // 참조형(reference type) 변수의 초기화
    }
    
    // 3. 복잡 초기화
    //    1) 초기화 블럭
    //     - 인스턴스(iv) 초기화 블럭: { }
    //   - 클래스(cv) 초기화 블럭: static { }
    class StaticBlockTest{
        static int[] arr = new int[10]; // 명시적 초기화
        static { // 클래스 초기화 블럭 - 배열 arr을 난수로 채움
            for(int i=0;i<arr.length;i++){
                arr[i] = (int)(Marh.random()*10)+1;            
            }
        }    
    }
    //  2) 생성자(iv)
    Car(String color, String gearType, int door) { // 매개변수 있는 생성자
        this.color = color;
        this.gearType = gearType;
        tihs.door = door;
    }
    ```
  <br/>
 
* **멤버변수의 초기화 시기와 순서**

  * 클래스 변수 초기화 시점: 클래스가 처음 로딩될 때 단 한번
  * 인스턴스 변수 초기화 시점: 인스턴스가 생성될 때 마다
  * cv → iv / 자동 → 간단 → 복잡 초기화 
