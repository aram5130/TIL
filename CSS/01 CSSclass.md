2021.09.06

------

## CSS

#### Cascading Style Sheets

위에서 아래로 흐르는(cascading) 방향으로 만든다.

룰 기반(Rule-based, 규칙)의 언어, 특정 요소와 특정 요소들의 집합의 스타일 규칙을 정의 한다.

```css
selector	h1 {
				color: red; - 속성(property): 값(value);
				font-size: 12px; - 선언(declaration)
				}       {  }선언블럭
```

- 주석(comments) 

  /* 내용 */ 형식으로 작성



2021.09.07

------

##### CSS 적용 방법

1. 내부 스타일(embedded)

   ```html
   <head>
       <style>
           h1 {
               color: red;
           }
       </style>
   </head>
   <body>
       <h1>hello!</h1>
   </body>
   ```

2. 인라인 스타일(inline)

   ```html
   <body>
       <h1 style="color:red">hello!</h1>
   </body>
   ```

3. 외부 스타일(external)

   ```html
   <head>
       <link rel="stylesheet" herf="style/main.css">
   </head>
   <body>
       <h1>hello!</h1>
   </body>
   ```

   ```css
   경로 - style/main.css
   h1 {
       color: red;
   }
   ```



- 캐스캐이딩 원칙

  1. **스타일 우선순위**

     - 동인한 스타일이라도 선언된 위치에 따라 우선순위가 결정된다.

       (브라우저 스타일 < 개발자 선언 스타일 < 사용자 구성 스타일)

     - 적용 범위가 적을 수록 우선시 된다.

       (tag 스타일 < class 스타일 < id 스타일 < inline 스타일)

     - 소스코드의 순서가 뒤에 있으면 덮어쓴다.

       

  2. **스타일 상속**

     - 부모 요소에 있는 스타일 속성이 자식 요소로 전달된다.

       자식 요소에서 재정의 할 경우, 부모의 스타일을 덮어쓴다.

     - 상속되지 않는 속성도 있다. ex)배경 이미지, 배경 색 등

       

#### 선택자의 종류

- 주요 선택자

  1. Type selector(요소 선택자)

     

     ```css
     h1 {
         color: red;
     }
     ```

  2. ID selector (전역 속성, 태그에 id 값을 부여해서 사용)

     ```css
     #welcome-title {
         color: blue;
     }
     ```

     

  3. Class selector (전역 속성, 태그에 Class 값을 부여해서 사용)

     ```css
     .movie-title {
         color: tomato;
     }
     ```

- 속성 선택자

  Attribute selector(속성/특성 선택자)

  1. [attr]

     ```css
     a[target] {
         color: red;
     }
     ```

  2. [attr=vlaue]

     ```css
     a[href="http://example.org"] {
         color: blue;
     }
     ```

     ```css
     input [type="submit"] {
         color: orange;
     }
     ```

  3. [attr^=vlaue] 

     지정한 문자열로 시작하는 값을 포함하는 요소를 선택

     ```css
     a[href^="https://"] {
         color: silver;
     }
     ```

  4. [attr$=vlaue]

     지정한 문자열로 끝나는 요소를 선택

     ```css
     a[href$=".com"] {
         color: tomato;
     }
     ```

  5. [attr*=vlaue]

     지정한 문자열을 포함하는 요소를 선택

     ```css
     a[href*="example"] {
         color: powderblue;
     }
     ```

  #### Pseudo-Class selector(가상 클래스 선택자)

  1. [first-child]

     지정 선택자의 첫번째 자식요소를 선택

     ```css
     li:first-child {
         color: ;
     }
     ```

  2. [last-child]

     지정 선택자의 마지막 자식요소를 선택

     ```css
     .movie:last-child {
         font-size: 32pt;
     }
     ```

  3. [nth-child] 

     지정 선택자의 자식요소의 대상(숫자)를 선택

     ```css
     span:nth-child(3) {
         color: hotpink;
     }
     ```


------

#### type

1. [first-of-type]

   특정 타입의 첫번째 요소를 선택

   ```css
   p:first-of-type {
       color: ;
   }
   ```

2. [last-of-type]

   특정 타입의 마지막 요소를 선택

   ```css
   .movie:last-of-type {
       font-size: 32pt;
   }
   ```

3. [nth-of-type] 

   특정 타입의 요소 대상(숫자)를 선택

   ```css
   li:nth-of-type(3) {
       color: hotpink;
   }
   ```

------

1. [not]

   특정 요소를 제외 

   ex)input태그 중에서 class="pw"를 가진 요소를 제외하고 나머지 요소들에 대해스타일을 적용한다. type=""도 적용 가능. 

   input:not( type="password") {}

   ```css
   input:not(.pw) {
       background-color: indianred;
   }
   ```

2. [link] / [visited]

   특정 타입의 요소 대상(숫자)를 선택하여 컬러를 넣어줌

   link : 방문하지 않은 링크에 설정한 컬러가 노출

   visited : 방문한 링크에 설정한 컬러가 노출

   ```css
   a:link {
       color: tomato;
   }
   a:visited {
       color: yellowgreen;
   }
   ```

3. [hover] / [active] / [focus]

   hover : 마우스를 올리면 지정한 스타일링으로 변경

   active : 마우스를 클릭하고 있을 때(활성화), 지정한 스타일링으로 변경

   ​			(:link, :visited, :hover)의 순서로 적용

   focus : 특정 요소에 포커싱이 되었을 때, 지정한 스타일링이 적용된다.

   ​			탭키를 사용하여 지정하거나, 입력하기 위해 선택했을때

   ```css
   input[type="button"]:hover {
       background: teal;
   }
   input[type="button"]:active {
   	background: red; 
   }
   input[type="button"]:focus {
   	background: blue; 
   }
   ```

4. [enabled] / [disabled] / [checked] 

   enabled : 활성화 되어있는 요소들에 스타일링을 지정.

   disabled : 비활성화 되어있는 요소들에 스타일링을 지정.

   checked : 체크되어 있는 요소에 스타일링을 지정. (radio, checkbox에 사용 가능)

   ```css
   input[type="text"]:enabled {
       background-color: skyblue;
   }
   input[type="text"]:disabled {
   	background: tomato; 
   }
   input[type="radio"]:checked {
   	outline: 2px solid red;
   }
   ```

   

   2021.09.08

   ------

   #### Pseudo-Element Selector (가상 요소 선택자)

   1. [before] / [after]

      before : 존재하지 않는 가상의 요소(content)에 적용되어 있음. 단순하게 꾸미기 위한 가상요소로 텍스트로 인식되지 않음. (드래그 불가), 앞에 위치

      after : before 와 동일한 기능, 뒤에 위치

      ```css
      .movie::before {
          content: 'MOVIE';
          color : teal;
      }
      .favorite::before {
          content: '💛';
          color : teal;
      }
      ```

   2. [first-letter] / [first-line] / [selection]

      first-letter : 첫번째 글자에 스타일링 적용.

      first-line : 브라우저에서 보이는 첫번째 줄에 스타일링 적용.

      selection : 드래그 하면 적용된 스타일링이 나타남.

      ```css
      .lorem::first-letter {
          color: red;
          font-size: 30pt;
      }
      .lorem_two::first-line {
          color: red;
          font-size: 30pt;
      }
      .lorem_::selection {
          color: white;
          background-color: blue;
      }
      ```

   

   #### Selector Combination (선택자 결합)

   1. 하위 선택자 결합(공백) : 두가지 요소를 선택해서 사용, 스페이싱을 사용해서 구분.

      전체 문서가 아닌 입력한 요소로 범위가 좁혀짐.

      ```css
      ul li:last-of-type {
          color: red;
      }
      ```

   2. 자식 선택자 결합(>) : 바로 아래의 하위(자식) 요소를 선택

      ```css
      #list > li:last-of-type {
          color: tomato;
      }
      ```

   3. 형제 선택자 결합 : 

      - 일반 형제 선택자 결합 (~) : 지정한 요소의 아래에 위치한 요소를 지정.

        ```css
        .code ~ selector {
            color: teal;
        }
        ```

      - 인접 형제 선택자 결합 (+) : 바로 앞뒤에 있는 (붙어있는) 요소를 지정.

        ```css
        .red + div {
            color: yellow;
        }
        ```

   4. 그룹화(,) : 여러개를 한번에 적용시킬때

      ```css
      p, div, #list_a {
          color: yellowgreen;
          font-size: 25pt;
      }
      ```

   

   #### Universal Selector  (범용선택자)

    범용 선택자 (*) : 전체를 지정, 주로 css 초기화를 할때 사용했었음.

   ```CSS
   * {
       magin: 0 auto;
   }
   ```

   

   #### 상속 제어하기

   1. initial  : 부모로부터 상속받을 값이 없을 때, 브라우저 기본값으로 정함.

   2. inherit : 부모로부터 상속받을 값이 있을 때, 부모와 같은 값을 받음.

      ```css
      #parnet2 * {
          all: inherit;
      }
      ```

   3. unset : 속성을 자연스러운 값으로 초기화 함.

      *참고해서 좀 더 공부해보기*

      [https://developer.mozilla.org/ko/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance]: 

      

