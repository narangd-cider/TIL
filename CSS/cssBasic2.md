>**`(드림코딩)프론트엔드 개발자되기 입문편 강의`를 수강한 후 정리하였습니다.**

</br>

# CSS Basic 2
### 📌 Size unit
- Absolute
  - cm, mm, Q, in, pc, pt, px 
  - px 주로 사용
- Relative
  - em, ex, ch, rem, 1h, vw, vh, vmin, vmax, %
  - em, rem, vw, vh, % 주로 사용
 <br/><br/>

### 📌 Relative length units
- `em`
  - relative to parent element
  - An em is a unit in the field of typography, equal to the currently specified point size
  - Same for all typefaces at a given point size
  - 선택된 font-family에 상관없이 고정된 font size를 가지고 있음
  - 부모의 폰트 사이즈에 상대적으로 크기 계산
  <br/><br/>
    ```html
    <div class="parent"
      Parent
      <div class="child">Child</div>
    </div>
    ```
    ```css
    .parent {
    font-size: 8em;
    /* 16px * 8 = 128px */
    /* 800%와 동일 */
    }

    .chile {
      font-size: 5em;
      /* 128px * 0.5 = 64px */
      /* 50%와 동일 */
    }
    ```
- `rem`
  - relative to root element
  <br/><br/>
    ```html
    <div class="parent"
      Parent
      <div class="child">Child</div>
    </div>
    ```
    ```css
    .parent {
      font-size: 8em;
      /* 16px * 8 = 128px */
    }

    .chile {
      font-size: 5em;
      /* 16px * 0.5 = 8px */
    }
    ```
- `vw`, `vh`, `vmin`, `vmax`
  - viewport related
- `%`
  - parent related
  <br/><br/>

### 📌 100% vs 100vh
- `%`
  - container가 들어있는 부모 높이의 %를 채우겠다
- `vh`
  - 부모에 상관없이 item에 보이는 viewport height를 100% 쓰겠다 
  <br/><br/>

### 📌 unit 총정리
- 기준 1
  - 부모와 상관없이 브라우저에 따라서 반응
    - v*
    - rem
  - 부모 요소의 사이즈에 따라서 사이즈 변경
    - %
    - em
- 기준 2
  - 요소의 너비와 높이에 따라서 사이즈가 변경
    - %
    - v%
  - 폰트 사이즈에 따라서 사이즈가 변경
    - em
    - rem
    <br/><br/>
    ```css
    .title {
	    padding: 0.5em 0.5rem;
	    /* 상하: 폰트 사이즈에 맞게 조정 */
	    /* 좌우: 고정 */
	    background-color: burlywood;
    }
    ```
- 핵심
  - box size 관련
    - %
    - v*
    - flex
  - 요소의 폰트 사이즈
    - rem
    - em
<br/><br/>

### 📌 참고 사이트
- pxtoem.com