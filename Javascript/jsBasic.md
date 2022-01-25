>**`(드림코딩)자바스크립트 기초 강의`를 수강한 후 정리하였습니다.**

</br>

# Javascript Basic
### 📌 console 출력
  <br/>

  ```jsx
  console.log('hello world!');
  ```
  <br/>

### 📌 async vs defer
- `head` 안에 `script`  
- `body` 끝에 `script`
  - html 컨텐츠를 빠르게 볼 수 있음
  - javascript에 의존적인 경우 사용자가 정상적인 페이지를 보기 전까지는 fetching, execute ing 시간이 오래 걸림
- `head` + `async`
  - html이 parsing 되기 전에 js 실행
  - 다운로드가 먼저 된 js부터 실행
  - 순서에 의존적인 경우 좋지 않음    
- `head` + `defer` 
  - parsing하는 동안 필요한 js를 다 받아 놓음
  - 순서대로 js 실행 가능
  <br/><br/>
### 📌 'use strict';

  - JavaScript is very flexible
  - flexible === dangerous
  - added ECMAScript 5
  <br/><br/>
  
  ### 📌 참고 사이트
  - 공식 [Home - Ecma International (ecma-international.org)](https://www.ecma-international.org/)
  - 학습 [https://developer.mozilla.org/ko/](https://developer.mozilla.org/ko/)