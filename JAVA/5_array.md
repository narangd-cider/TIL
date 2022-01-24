>**`(남궁성의 정석코딩)자바의 정석 기초편 강의` 및 `Java의 정석 교재`를 학습한 후 정리하였습니다.**

</br>

# 5. Array
### 📌 배열(Array)
* **배열(array)이란?**

  * 같은 타입의 여러 변수를 하나의 묶음으로 다루는 것
  <br/><br/>
 

* **배열의 선언과 생성**

  * 배열을 다루기 위한 참조변수의 선
  * 배열 선언(배열을 다루기 위한 참조변수 선언)
    * 타입[ ] 변수이름; 혹은 타입 변수이름[ ]
  * 배열 생성(실제 저장공간 생성) 
    * 변수이름 = new 타입[길이];
  <br/><br/>
 
* **배열의 길이와 인덱스**

  * 인덱스는 각 요소에 자동으로 붙는 번호
  * 인덱스의 범위는 0부터 '배열길이-1'
  * 배열이름.length: 배열의 길이(int형 상수)
  * 배열은 한번 생성하면 실행하는 동안 길이를 바꿀 수 없음
  <br/><br/>
 
* **배열의 초기화**

  * 배열의 각 요소에 처음으로 값을 저장하는 것
  * 자동 초기화(int 타입은 0으로 초기화)
  * 배열은 한번 생성하면 실행하는 동안 길이를 바꿀 수 없음
  <br/><br/>
    ```java
    int[ ] score = new int[ ]{50, 60, 70, 80, 90};
    int[ ] score = {50, 60, 70, 80, 90}; // new int[] 생략 가능
    
    int[ ] score;
    score = {50, 60, 70, 80, 90} // 에러. new int[] 생략 불가능
    scroe = new int[ ]{50, 60, 70, 80, 90}; // OK
    ```
  <br/>
  
* **배열의 출력**

  * 배열의 각 요소에 처음으로 값을 저장하는 것
  * 자동 초기화(int 타입은 0으로 초기화)
  * 배열은 한번 생성하면 실행하는 동안 길이를 바꿀 수 없음
  <br/><br/>
    ```java
    int[ ] iArr = {100, 95, 80, 70, 60};
    System.out.println(iArr); // [I@14318bb와 같은 형식의 문자열 출력
    System.out.println(Arrays.toString(iArr)); // iArr의 모든 요소 출력 [100, 95, 80, 70, 60]
      
    char[ ] chArr = {'a', 'b', 'c', 'd'};
    System.out.prinln(chArr); // abcd가 순서대로 출력
    //문자형 배열의 경우 예외적으로 배열 이름으로 모든 요소 출력 가능
    ```
  <br/>

* **배열의 활용**

  * 총합과 평균
    * 배열의 모든 요소를 더해서 총합과 평균을 구함
  * 최대값과 최소값
    * 배열의 요소 중에서 제일 큰 값과 제일 작은 값을 찾음
  * 섞기 
    * 배열의 요소 순서를 반복해서 바꿈(숫자 섞기, 로또번호 생성)
  <br/><br/>
    ```java
    // 합계와 평균
    int sum = 0;
    float average = 0f;
    
    int[ ] score = {100, 88, 100, 100, 90};
    
    for (int i=0; i<score.length;i++){
        sum += score[i];
    }
    
    average = sum / flatO(score.length);
    
    System.out.println("총점: " + sum);
    System.out.println("평균: " + average);
    
    // 최대값과 최소값
    int[ ] score = {79, 88, 91, 33, 100, 55, 95};
    
    int max = score[0];
    int min = score[0];
    
    for(int i=1; i<score.length; i++){
        if(socre[i]>max){
            max = score[i];
        } else if(socre[i]<min){
            min = score[i];
        }
    }
    
    System.out.println("최대값: " + max);
    System.out.println("최소값: " + min);
    
    // 섞기(shuffle)
    int[ ] numArr = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
    System.out.println(Arrays.toString(numArr));
    
    for(int i=0; i<100; i++){
        int n = (int)(Math.random() * 10);
        int tmp = numArr[0];
        numArr[0] = numArr[n];
        numArr[n] = tmp;
    
    System.out.println(Arrays.toString(numArr));
    ```
  <br/>

### 📌 String 배열

* **String 배열의 선언과 생성**
  * String[] name = new String[3];
    * 3개의 문자열을 담을 수 있는 배열을 생성
    <br/><br/>

* **String클래스**

  * String 클래스는 char[ ]과 메서드(기능)을 결합한 것
    <br/><br/>

* **커맨드 라인을 통해 입력받기**

  * 커맨드 라인에 입력한 값이 문자열 배열에 담겨서 전달
    <br/><br/>
    ```java
    class Ex5_7 {
      public static void main(String[] args {
          System.out.println("매개변수의 개수:"+args.length);
          for(int i=0; i<args.length;i++){
              System.out.println("args[" + i + "] = \"" + args[i] + "\"");
          }
      }
      }
    
    /*
    C:\jdk1.8\work\ch5>java Ex5_7 abc 123 "Hello world"
    매개변수의 개수: 3
    args[0] = "abc"
    args[1] = "123"
    args[2] = "Hello world"
    
    C:\jdk1.8\work\ch5>java Ex5_7
    매개변수의 개수: 0
    */
    ```
  <br/><br/>

### 📌 다차원 배열

* **2차원 배열의 선언과 인덱스**
  * 테이블 형태의 데이터를 저장하기 위한 배열
  * 1차원 형태의 배열
  <br/><br/>
    ```java
    int[ ][ ] score = {
      {100, 100, 100},
      {20, 20, 20},
      {30, 30, 30},
      {40, 40, 40}
    };
    int sum = 0
    
    for(int i=0;i<socre.length;i++){
        for(int j=0j<score[i].length;j++){
            System.out.printf("score[%d][%d]=%d%n", i, j, score[i][j]);
            
            sum += socre[i][j];
        }
    }
    
    System.out.println("sum=" + sum);
    ```
    <br/>

* **Arryas 클래스로 배열 다루기**
  * 비교와 출력 
    * [1차원 배열] equals( ), toString( ) 
    * [2차원 이상 배열] deepEquals( ), deepToString( )
  * 복사 - copyOf( ), copyOfRange( )
  * 정렬 - sort( )
  <br/><br/>
    ```java
    // 비교와 출력
    int[] arr = {0, 1, 2, 3, 4};
    int[ ][ ] arr2D = {{11, 12}, {21, 22}};
    
    System.out.println(Arrays.toString(arr)); // [0, 1, 2, 3, 4]
    System.out.println(Arrays.deepToString(arr2D)); // [11, 12], [21, 22]]
    
    String[ ][ ] str2D = new String[ ][ ]{{"aaa", "bbb"}, {AAA", "BBB}};
    String[ ][ ] str2D2 = new String[ ][ ]{{"aaa", "bbb"}, {AAA", "BBB}};
    
    System.out.println(Arrays.eqauls(str2D, str2D2); // false
    System.out.println(Arrays.deepEquals(str2D, str2D2); // true
    
    // 복사
    int[ ] arr = {0, 1, 2, 3, 4}
    int[ ] arr2 = Arrays.copyOf(arr, arr.length); // arr2 = [0, 1, 2, 3, 4]
    int[ ] arr3 = Arrays.copyOf(arr, 3); // arr3 = [0, 1, 2]
    int[ ] arr4 = Arrays.copyOf(arr, 7); // arr4 = [0, 1, 2, 3, 4, 0, 0]
    int[ ] arr5 = Arrays.copyOf(arr, 2, 4); // from 2 to 4 = 2부터 3까지. arr5 = [2, 3]
    int[ ] arr6 = Arrays.copyOf(arr, 0, 7); // arr6 = [0, 1, 2, 3, 4, 0, 0]
    
    // 정렬
    int[ ] arr = {3, 2, 0, 1, 4};
    Arrays.sort(arr); // 배열 오름차순 정렬
    System.out.println(Arrays.toString(arr)); // [0, 1, 2, 3, 4)
    ```
 



