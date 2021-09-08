2021.09.08

------

## 폰트 / 텍스트

#### 폰트 관련 속성

1. `font-size` : 글자 크기 (단위를 붙여서 사용, 16px 기본값)
2. `font-style` : 폰트의 생김새(주로 italic을 사용)
3. `font-weight` : 폰트의 굵기
4. `font-family` : 글꼴을 변경하기 위해서 사용.
5. `line-height` : 줄의 높이. 폰트에 따라서 높이가 다를 수 있기 때문에 UI적인 용도로 사용할 수 있다. 



#### font 와 단축 속성

- `font-size` , `font-family` 는 **필수요소**

- `font-style` , `font-variant` , `font-weight` , `line-heirgt`

  ```css
  **동일한 기능**
  .text {
      font-size: 20px;
      font-family: 'Times new Roman', Times, serif;
  }
  .text {
      font: 20px 'Times new Roman', Times, serif;
  }
  ```

  **`font-style` / `font-weight` 는 `font-size` 앞에 위치, `line-heirgt`는 뒤에 위치하고 `font-family`는 가장 뒤에 위치.**

------

기본 값을 nomal로 하며, nomal(기본값)에 입력한 값만큼이 더해져서 보여짐.

- `letter-spacing` : 자간
- `word-spacing` : 단어 사이의 간격



#### 텍스트 관련 속성

1. `text-align` : 정렬(center, left, right)

   블럭 요소에 적용 가능. 인라인 요소에는 적용이 불가능.

   인라인 요소에 적용해야 할 때에는 부모 요소를 블럭 요소로 지정해서 사용 가능.

2. `text-indent` :  들여쓰기 기능. %퍼센트 값 사용 가능. 블럭 요소에 적용 가능. 인라인 요소에는 적용이 불가능.

3. `text-decoration` : 단축 속성. 글씨의 장식을 지정함.

   [https://developer.mozilla.org/ko/docs/Web/CSS/text-decoration]: 

4. `word-break` : 콘텐츠 박스 밖으로 오버플로우 할 때 줄 바꿈을 지정함.

5. `text-transform` : 한국어 적용X, capitalize(앞글자 대문자) / lowercase(소문자) / uppercase(대문자)

