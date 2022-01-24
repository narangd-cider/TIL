>**`(드림코딩)프론트엔드 개발자되기 입문편 강의`를 수강한 후 정리하였습니다.**

</br>

# PWA
### 📌 PWA 개요
- `PWA`가 뜨는 추세이며 계속 성장세를 이어 나갈 것
- 트위터, 우버, 핀터레스트, 유튜브, 틱톡, 스포티파이 등 많은 기업들이 이미 `PWA`의 강력한 잠재력을 알아보고 `PWA` 시장에 뛰어들어 성공적으로 런칭
- 새롭고 강력한 소프트웨어 앱을 만드는 방식
- HTML, CSS, JavaScript를 이용해서 만든 웹앱을 모던한 웹 브라우저 `APIs`와 결합해서 크로스 플랫폼에서 동작하는 어플리케이션을 만들 수 있음
- 이미 만든 웹사이트나 웹 어플리케이션이 있다면 몇 가지만 추가하면 손쉽게 데스크탑 / 모바일에서 동작하는 어플리케이션을 만들 수 있음
<br/><br/>

### 📌 Native App / Web App 장단점
- Native App
    - 안드로이드나 아이폰처럼 특정한 플랫폼에서 동작하는 `Native App`은 플랫폼에서 제공하는 다양한 `API`를 사용자에게 다양한 기능을 제공
    - `App store`를 이용해서 설치해야하며,  해당 플랫폼에서만 사용할 수 있다는 단점
- Web App
    - 반대로 브라우저에서 동작하는 웹앱은 플랫폼에 상관없이 브라우저만 있다면 사용할 수 있어 사람들이 쉽게 접근해서 사용할 수 있다는 장점
    - 네이티브앱처럼 플랫폼 자체의 `API`를 사용할 수 없다는 단점
- `PWA`는 `Web App`(접근성) + `Native App`(플랫폼 API를 사용) 장점 결합
<br/><br/>

### 📌 new class of web apps PWA
- responsive web design
- service workers
- app manifest
- push notification
- native app-like capabilities
<br/><br/>

### 📌 Project Fugu
- web capabilities project
- google / microsoft / intel
<br/><br/>

### 📌 PWA 제약사항
- 새롭게 추가되는 브라우저 API들은 특정 브라우저나 예전 브라우저 버전에서 사용 불가능
<br/><br/>

### 📌 참고 사이트
- PWABuilder 
  - [https://www.pwabuilder.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbEprc0Q2dDlHQXFrbktTeENKcjVWQ00zc2ZmQXxBQ3Jtc0tsRDUwOWFGaVUxZWNxc1VzY3drRWd0Wnd4U3NUajdZdnUxLUxoOTJUSERoNzRSSTNDU0pkQnVmaTF0N3hSYTRPSnJrQlRDX04zS0lqaXRPV1JVZlF1bENvSWhNckVzZmFsa0YtemFYN090ZmxoNDloNA&q=https%3A%2F%2Fwww.pwabuilder.com%2F)
- Workbox
  - [https://developers.google.com/web/tools/workbox](https://developers.google.com/web/tools/workbox)
- Maskable
  - [https://maskable.app/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa29EOXB6Wi1SNmdnTEdCNG9GZDVPVHJCM09EZ3xBQ3Jtc0trMmhYMnhGaHJaMWRFZFA4WnZRbm1sQUlDSGl2QTBGWENxS085b0VnQUhhdGlOOXU2b2VwVnhFOGRMSzVDamo4dFlaajg5MVdpVkdZVWo2Z3UwRkRRRnhQQjhEcHZwZGJKUUI5ZThhLU4zdTRBVzNCMA&q=https%3A%2F%2Fmaskable.app%2F)
- Web.dev
  - [https://web.dev/install-criteria/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbkxxTk4xbVdtM0FHVkk5aW5ySFU2TUw0eU90Z3xBQ3Jtc0ttYk16alJqa1FvcE9aRWx5SWY2YXUzUDNIaEYxMHNTUFg4M1BqZk1pc1I1SDFXdTlzRDJFZ3hMNEVfRGtzM0dwZXYtOU56d016T05UZFVPc3hYandSUnRlbW13MkJlWFotNW9kQTA0cFg2S21FcTdPcw&q=https%3A%2F%2Fweb.dev%2Finstall-criteria%2F)
- PWABuilder Github
  - [https://github.com/pwa-builder/pwabuilder-web/blob/V2/src/assets/next-steps.md](https://github.com/pwa-builder/pwabuilder-web/blob/V2/src/assets/next-steps.md)
<br/><br/>

### 📌 PWA 필요 요소
- 웹코드로 만든 웹사이트나 웹 어플리케이션
- HTTPs를 이용해서 서비스 제공
- Application Manifest
    - JSON으로 된 Text.file 웹 어플리케이션에 대한 정보가 담겨져 있는 파일
- Service Worker
    - JavaScript로 작성
    - 어플리케이션에서서버와 데이터를 주고받을때 중간에서 그 모든 요청들을 통제하고 관리
