>**`(드림코딩)프론트엔드 개발자되기 입문편 강의`를 수강한 후 정리하였습니다.**

</br>

# API
### 📌 Application Programming Interface(API)

- 각각의 운영체제에서 동작하기 위한 어플리케이션을 만들기 위해서는 운영체제에서 제공하는 `APIs`를 이용해서 만들 수 있음
- 다양한 기기에서 서버에 있는 데이터를 읽고 쓰기 위해서는 서버에서 제공하는 `Web API`들을 이용하고 처리할 수 있음
- `Web API`뿐만 아니라 라이브러리나 프레임워크에서 우리가 이용할 수 있는 클래스나 함수들을 `API`라고 부름
  - 외부에서 가져오는 프로젝트 내부에서 쓰여지고 있는 클래스나 모듈이 있다면 Calculator에서 제공하는 함수 이용(= 인터페이스 이용
    = `API` 이용) 이라고 말할 수 있음        
- 내부의 구현 사항을 잘 숨겨두고 외부에서 사용하는 사람이 필요한 것만 노출해둔 것
<br/><br/>   
### 📌 Web API

- **HTTP**

  - `Web API`를 어떻게 디자인해서 만들지 정의하는 것
  - 네트워크에서 기기들간에 의사소통 해나가는 규격 사항
  <br/><br/>

- **SOAP vs REST**

  - `SOAP`
    - Simple Object Access Protocol
    - 이전에는 모든 네트워크 요청과 반응을 `HTML`처럼 생긴 `XML`이라는 데이터 포맷에 저장해서 주고 받음
  - `REST`
    - Representational state transfer
    - 요즘에 보편적으로 많이 사용
    - Post(create) / Get(read) / Put(update) / Delete (delete)
      - Get을 이용해서 유저에 대한 정보 요청
      - 서버로부터 유저에 대한 데이터를 JSON이라는 포맷을 통해서 받아올 수 있음
      - 서버에서 제공하는 Web API를 통해 서버에 있는 데이터를 읽어오고나 업데이트 할 수 있음
  <br/><br/>

- **Open API, Public API**

  - 회사 내부에서 사용하는 Web API를 외부의 다른 개발자가 이용할 수 있도록 공개적으로 오픈
  - 이런 오픈된 API를 이용해서 많은 개발자들이 독창적이고 재미있는 어플리케이션을 만들 수 있음
  - 궁극적으로 회사, 서비스 커뮤니티에 많은 기여
  <br/><br/>

- **참고 사이트**
  - public-apis 1
    - [https://github.com/public-apis/public-apis](https://github.com/public-apis/public-apis)
  - public-apis 2
    - [https://public-apis.xyz/page/1](https://public-apis.xyz/page/1)
  - PHY
    - [https://developers.giphy.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmNTZmxGZWJDWDBHRjdCSnNXV3R4dHFpVFZLd3xBQ3Jtc0ttbHRlb3ZNaUxiOWdESXNwVWRYM2Y5U1VVZ0ZxWjRoSkdMdnE5bkNCa1o5R0lYRmpHazNldXlMaC1EQVhOb0Q4ZDVXdWhzTXRXbHBDTjdieVUxamwtU1dlcENMbnpiNzZLZDI1NnR2M2FGSXA3SGg0RQ&q=https%3A%2F%2Fdevelopers.giphy.com%2F)
  - otify
    - [https://developer.spotify.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa3RycFJaMGtKRWFJTE5zb1lDZFdFbWk5TG96QXxBQ3Jtc0trUDlCSTVwYkdFeHNBQ2ZuUmJYaTFUSnNlaW1aUndKMkRacXZUamxXWmU0Tm5OMjVrNmFxQ0dkbG1xOHlGMUQ3aHJ2Q2l4SzRaQVlLMHpvS0hDZktYcXdpWlREb3dLSGNRR09iS0JkTFVuMy03eU92NA&q=https%3A%2F%2Fdeveloper.spotify.com%2F)
  - amam
    - [https://developer.edamam.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbURQcTJ0STNnV0otemhMcVEzUllMcWp5c0JOQXxBQ3Jtc0trN01lQWR2OFJwcjhhWHlTOU5KcTNfUTNQTXRTenJPWE82amxxbms4V3lKMW1XU09UQlFDbnBqR2RaOFBnemFmRGtVMGc5UDVKc3IyeWUyUC0zRUxLbkFsa1NLczlBSVh2UHh3SHU3UUluMlBfOElfYw&q=https%3A%2F%2Fdeveloper.edamam.com%2F)
  - meme
    - [http://apimeme.com/?ref=apilist.fun](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbExmM2otemhqbW5UbkFVT2xnYU5XVTVBNEdGd3xBQ3Jtc0trWUhWQWJQODRSa2g2LUVsMmUyTG9IcjVWYnQyX3M0S2VSTk9LVThBRW1ra25nUjBxODh1ckNiUk41WFp5UXRZMGtoVV81UG5EN1F4UUhlNElLVU96ZjNWUm04Z3BBNV9iUzVlc3BJS1ZzcGJIVzVuYw&q=http%3A%2F%2Fapimeme.com%2F%3Fref%3Dapilist.fun)
  - 증권
    - [https://www3.kiwoom.com/error.html](https://www3.kiwoom.com/error.html)
  - 공공 데이터
    - [https://www.data.go.kr/tcs/dss/selectDataSetList.do](https://www.data.go.kr/tcs/dss/selectDataSetList.do)
  - 카카오
    - [https://developers.kakao.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbEJmdmFYLU51aHE3MmlYelRoRERIdFZCajVtUXxBQ3Jtc0trOXAwb3o4eFphYzBuR0kyNWczZkU1enp4bGF5dXNmUWduVjd4WUYwUWxxaktUenFTdFhoVEZRM2VSOFhSOG5VU1plYWRwTE1uOHNZMm1ET29Ea3UzWm1BSEtpQm11VU5CZm54THFIMkw3ODU0QlBXWQ&q=https%3A%2F%2Fdevelopers.kakao.com%2F)