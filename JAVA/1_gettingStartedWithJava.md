>본 게시물은 남궁성의 정석코딩 자바의 정석 기초편 강의 및 Java의 정석 교재를 학습한 후 정리하였습니다.

</br>

# 1. getting started with Java
### 📌 Java Programming Language

* 자바란

  * 객체지향 프로그래밍 언어
  * 컴퓨터 프로그램 만들 때 사용: PC / Web / 모바일 App, 빅데이터, 게임 등
  * 실행환경(JRE) + 개발도구(JDK) + 라이브러리(API)
  <br/><br/>

* 자바의 역사

  * JDK 1.0(1996): 자바개발도구
  * J2SE 1.2(1998): Java2
  * J2SE(Standard edition) / J2ME(micro edition) / J2EE(enterprise edition) 
  * J2SE 5.0 (2004) 
  * Java SE 8 (2014) : 6개월마다 버전 업데이트 중
  * Java SE 13 (2019)
  <br/><br/>

* 자바언어의 특징

  * 배우기 쉬운 객체 지향 언어 = 프로그래밍 언어 + 객체 지향 개념
  * 자동 메모리 관리: Garbage Collector
  * multi thread 지원
  * 풍부한 library로 쉽게 개발 가능
  * OS에 독립적
  <br/><br/>

* JVM(Java Virtual Machine)

  * 자바 프로그램이 실행되는 가상 컴퓨터
  * 한번 작성하면, 어디서든 실행(Write once, run anywhere)
  * Java Application ↔ JVM ↔ OS(Windows) ↔ 컴퓨터(하드웨어)
  * 일반 Application ↔ OS(Windows) ↔ 컴퓨터(하드웨어)
  <br/><br/>

### 📌 자바개발환경 구축하기
* 자바 개발도구(JDK) 설치하기

  * jdk 설치 > bin 폴더 path 등록 > 이클립스 설치
  <br/><br/>
* Java API문서 설치하기

  * JAVA API: java로 프로그램을 만드는데 필요한 주요 기능 미리 제공
  * JAVA API 문서: JAVA API가 제공하는 기능에 대한 상세한 정보 제공(html 파일)
  * www.oracle.com에서 다운로드
  * 구글에 java api download 검색 > docs 폴더를 jdk 폴더 안에 위치시키기
  <br/><br/>

### 📌 자바로 프로그램 작성하기
* 이클립스 단축키

  * Ctrl + Shift + L: 단축키 전체 목록
  * Ctrl + (+, -): 글자 크기 조절
  * Ctrl + D: 한줄 삭제
  * Ctrl + Alt + Down: 행 단위 복사
  * Alt + Shift + A : 멀티 컬럼 편집
  * Alt + (Up, Down) : 행 단위 이동
  * Tap : 들여쓰기  
  * Shift + Tap : 내어쓰기
  * Ctrl + I : 자동 들여쓰기
  * Ctrl + Sspace : 자동인식
  * 충돌 발생 시 Window > Preferences > general > keys > copy line 변경
  * Java > Editor > Templates > sysout > sop 변경 
  * content Assist > Auto activation triggers for java > a-z까지 등록