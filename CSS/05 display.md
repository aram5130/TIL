2021.09.15

------

## display

1. `display: inline;` : span... 영역 사이즈가 내부 콘텐츠로 결정된다

   margin과 padding 의 top/bottom

   여러 요소가 가로로 배치된다

2. `display: block;` : div... 영역의 크기를 width, height 지정할 수 있다.

   width값을 지정하지 않으면 가로 전체를 차지한다

   여러 요소가 세로로 배치된다.

3. `display: inline-block;` : input... 영역의 크기를 width, height 지정할 수 있다.

   여러 요소가 가로로 배치된다

   margin과 padding을 모두 지정할 수 있다.

   여러 요소가 가로로 배치된다.

요소를 없애는 방법

1. `display: none;` : 요소를 보이지 않도록 함. 레이아웃에서 아예 없어짐
2. `visibility: hidden; ` : 요소를 숨김. 레아아웃 자리는 남아있지만 보여지지만 않음.

##### float

1. `float: none;` : 기본값.
2. `float: left;` : 요소의 왼쪽 방향으로 흐르게 하기 위해서 사용
3. `float: right;` : 요소의 오른쪽 방향으로 흐르게 하기 위해서 사용

##### position

- Normal Flow(일반대열) : 요소의 레이아웃을 변경하지 않았을때 자동적으로 배치되는 방법. 기본적인 배열

1. `position: static;` : 일반적인 배열(기본값), top / bottom / left / right 사용불가

2. `position: relative;` : 일반적인 배열을 따르지만, **자기자신을 기준**으로 이동한다. top / bottom / left / right 사용 (음수값도 사용 가능)  top / bottom이나 left / right을 함께 사용 할 수 없다.

3. `position: absolute;` : 일반적인 배열을 제거한다. 페이지 레이아웃에 배정되지 않는다. **가장 가까운 위치의 조상요소(static이 아닌 조상요소)**에 대해 적용 된다. 

   **absolute를 사용하고 싶을때, 위치 지정 조상 요소에 relative를 적용시켜 사용하는 경우가 많다.**

4. `position: fixed;` : 일반적인 배열을 제거한다. 페이지 레이아웃에 배정되지 않으며 **뷰포트를 기준**으로 배치된다. 뷰포트 자체에 위치가 고정되어 있음. (네비게이션바, 화면에 고정되어야하는 아이콘 등에 사용)

5. `position: sticky;` : 일반적인 배열을 따르지만, 특정 위치에서 스크롤되는 조상에 위치. 스크롤해서 조상의 위치가 바뀌면 그대로 따라다니듯이 뷰포트에 보여진다. 

overflow : 

1. `overflow: visible;` : 기본값. 넘치는 값이 그대로 나온다.
2. `overflow: hidden; ` : 넘치는 값이 잘려서 보이지 않는다.
3. `overflow: scroll; ` : 적용한 요소에 마우스를 올리고 스크롤 할 경우 스크롤바가 나타나서 넘치는 값을 확인할 수 있다. 별도의 박스가 생성됨.
4. `overflow: auto ;` : 브라우저가 내용의 길이에 따라서 자동으로 값을 선택함.

z-index : 위치 지정 요소

1.  `z-index: auto; ` : 기본적인 쌓임의 순서를 따른다. 값이 0..
2. `z-index: 숫자; ` : 배열 순서를 지정할 수 있다. 최상위에 올라와야 하는 경우 큰 값으로 주어 가장 위로 올라오게끔 사용할 수 있다.

