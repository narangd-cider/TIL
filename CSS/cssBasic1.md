>**`(드림코딩)프론트엔드 개발자되기 입문편 강의`를 수강한 후 정리하였습니다.**

</br>

# CSS Basic 1
### 📌 Cascading Style Sheet
- Author style
- User Style
- Browser
- `!important` 연결고리는 무시하고 내가 제일 중요해!
  - 이미 구조가 잘못 설계 되었을 확률이 높기 때문에 가능하면 사용하지 않는게 좋음 
  <br/><br/>
  
### 📌 Selectors
- MDN CSS Selectors
  - [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)
- Select the plates
  - [https://flukeout.github.io/](https://flukeout.github.io/)
- Universal `*`
- type `Tag`
- Id `#id`
- class `.class`
- state `:`
- Attirbute `[]`
- Styling
  - CSS Reference: [https://developer.mozilla.org/en-US/docs/Web/CSS/Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
  - CSS Properites Reference: [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference)
    <br/><br/>   
    ```css
    button: hover {
    	/* 마우스를 올린 경우 */
    }
    a[href^=”naver”] {
    	/* naver로 시작하는 경우 */
    }
    a[herf$=”.com”] {
    	/* com으로 끝나는 경우 */
    }
    li#special {
    	/* li 태그 중 id가 special인 경우 */
    }
    .red {
    	width: 100px;
    	height: 100px;
    	padding: 20px 20px 20px 20px; <!-- top, right, bottom, left -->
    	padding: 20px 20px <!-- top and bottom, right and left -->
    	margin: 20px
    	background : yellow;
    ```
    <br/>

### 📌 Display
- [https://developer.mozilla.org/en-US/docs/Web/CSS/display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- `inline-block`
- `inline` 
- `block`
    <br/><br/>    
    ```css
    div, span{
    	width: 80px;
    	height: 80px;
    	margin: 20px
    }
    
    div {
    	/* default: Block level */
    	background: red;
    	display: inline-block;
    }
    
    div {
    	/* default: Block level */
    	background: red;
    	display : inline <!-- contents만을 꾸며줌 -->
    }
    
    span {
    	/* default: Inline level */
    	background: Blue;
    	display: block
    }
    ```
    <br/> 

### 📌 Position
- [https://developer.mozilla.org/en-US/docs/Web/CSS/positio](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
- `static` (default)
  - html에 정의된 순서
- `relative`
  - 원래 있어야 할 item 기준으로 이동
- `absolute`
  - item과 가장 가까이에 있는 container 기준으로 이동
- `fixed`
  - container에서 벗어나 window 기준으로 이동
- `sticky`
  - 원래 있어야 할 자리 + scrolling해도 원래 있던 자리 그대로 있음
<br/><br/>

### 📌 CSS 추세
- 기존에는 Bootstrap이나 JQuery같은 library를 많이 사용
  - css 및 javascript에 강력한 기능이 없었음
  - borwser에서 제공되는 API 빈약
- 현재는 최신 기능을 활용한 CSS 작업 진행
- 그러나, 새로운 기능을 쓸 때 호환성 여부 검사 필요 
  - [https://caniuse.com](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa0h6OURINzBMRzJtS3MwaE1rNmk4TnBBSlAxQXxBQ3Jtc0trNGxOZzhHdTRQYzNzWlZ3cDhXTmM4dER2R2Nuam5CWGY3Q3ZrTldBVkhSLXRyczduT0loT18tUVlJejlBWC05eTUwUEw0TC1PUWlyUHNGVkpaaEdWUVUzTEY1dER5MVNzSE1qRXMzVU9jcFRONGJUNA&q=https%3A%2F%2Fcaniuse.com%2F)
- 결론적으로 최신 CSS 작업 및 호환성 검사 + PostCSS 프레임워크 활용