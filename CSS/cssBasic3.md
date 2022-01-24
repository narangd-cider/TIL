>**`(드림코딩)프론트엔드 개발자되기 입문편 강의`를 수강한 후 정리하였습니다.**

</br>

# CSS Basic 3
### 📌 Flexbox
- 등장배경
  - 기존에는 layout을 만들기 위해 `Position`, `float`, `table` 활용
  - `float`의 경우 이미지와 text를 배치하려는 목적을 가진 태그
  - 그러나 순수 목적에 어긋나게 사용하다보니
    - box안에 item을 수직-가운데 정렬
    - item의 사이즈에 상관없이 동일한 간격 및 size로 사이즈에 배치
    - 박스를 동일한 높이로 두는 것 등 어려움이 많았다
  - 이제는 `Flexbox`를 활용하여 `box`와 `item`을 행 또는 열로 자유자재로 배치할 수 있게 되었다
  <br/><br/>

- Concept
  - `box` 및 `item`에 적용할 수 있는 속성값들이 존재
  - `main axis` 및 `cross axis` 존재
    - 중심축을 수평, 수직으로 두나에 따라 반대축이 바뀐다 
  <br/><br/>

- box 속성값
  - `flex-direction`
    - row(default)
    - row-reverse
    - column
    - column-reverse
  - `flex-wrap`
    - nowrap(default)
    - wrap
    - wrap-reverse
  - `flex-flow`
    - /* flex-flow: column nowrap; */ 
  - `justify-content`: main-axis 아이템 배치
    - flex-start
    - flex-end
    - center
    - space-around
    - space-evenly
    - space-between
  - `align-items`: main.axis 고정 + cross axis 위치
    - center
    - baseline
    <br/><br/>
- item 속성값
  - `order`
    - 현업에서 거의 사용하지 않음
  - `flex-grow`
    - container를 꽉 채우려고 item이 늘어남
    - flex-grow를 설정하지 않은 경우, 자신의 고유한 크기 유지
    - 컨테이너가 지나치게 줄어들면 조금씩 작아지는 형태
  - `flex-shrink`
    - container가 점점 줄어들 때 item이 작아지는 정도
  - `flex-basis`
    - auto
      - grow 및 shrink에 지정된 대로 변경
    - %
      - grow 및 shrink를 지정하지 않은 경우 container의 width에 따라서 크기 변경
  - `align-self`
    - container에 벗어나 아이템별로 정렬
  <br/><br/>

### 📌 참고 사이트
- color tools
  - https://material.io/resources/color/#!/?view.left=0&view.right=0
- MDN Flexbox
  - [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
- CSS Tricks for Flexbox
  - [https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- Flexbox 연습 게임
  - FLEXBOX FROGGY