2021.09.02

------

# 오늘의 정리



## 폼요소

사용자에게 정보를 입력할 수 있는 장치를 제공하는 것, 입력한 정보를 다른 페이지나 서버로 전송하는 역할을 한다. (일부의 동적인 기능 수행)

- `<form>` 폼

  action : 양식 데이터를 처리 할 프로그램의 URI (입력된 정보를 다른 페이지나 서버의 주소를 넣음, 목적지의 주소가 들어간다-)

  method : 양식을 제출할 때 사용할 HTTP 메소드

  - post(많이 사용할 것) :데이터를 서버로 제출하여 추가, 수정하기 위해 사용 (URL에 데이터가 나타나지 않는다)

  - get : 원하는 데이터를 가져와서 조회하기 위해 사용 (URL에 데이터가 나타남)

  - dialog

    ```html
    <body>
        <!-- url에 name과 입력값(데이터)노출 -->
        <form action="" method="GET">
            <input type="text" name="test">
        </form>
        <!-- url에 입력값(데이터)보이지 않음 -->
        <form action="" method="POST">
            <input type="text" name="test">
        </form>
    </body>
    ```

- `<label>`

  input에 설명을 해주는 레이블, 어떤 정보를 담아야 하는 것인지 텍스트로 나타내주는 것이 좋다. 

  ex) **로그인** : [입력칸]  /  **비밀번호** : [입력칸]

- `<input>`

  정보를 입력 할 수 있는 칸. 단순한 입력칸 이외에도 다양한 정보를 받을 수 있는 양식을 가지고 있다. 

  ```html
  <body>
      <form action="" method="GET">
          <div>
              <label for="fruitname">과일이름 : </label>
              <input type="text" name="fruit" id="fruitname">
              <button type="submit">제출</button>
          </div>
          <div>
              <label>색이름 : </label>
              <input type="text" name="color" id="colorname">
              <button type="submit">제출</button>
          </div>
      </form>
  </body>   
  ```

  

- `<fieldset>`

  웹 양식의 여러 컨트롤과 레이블 `<label>` 을 묶을 때 사용, 스타일만을 생각한다면 css만드는 것이 가능하지만, 정확한 역할을 가지고 있다면   `<fieldset>` 과 `<legand>`(범례) 를 사용! (시멘틱적 측면)

  *`<legand>` 부모 요소를 `<fieldset>` 으로 두고, 안에 있는 요소들을 박스로 묶어서 보여준다.

  `<fieldset>` 을 사용할 경우 그 안에 있는 요소들을 한번에 제어할 수 있다.

  ​		ex) `disabled` : 지정한 모든 자손 컨트롤을 비활성화 한다.

  ```html
  <form>
      <fieldset>
          <legend>범례 1</legend>
            <div>
              <label for="fruitname">과일이름 : </label>
              <input type="text" name="fruit" id="fruitname">
            </div>
            <div>
              <label for="colorname">색 이름 : </label>
              <input type="text" name="color" id="colorname">
            </div>
          	<button type="submit">제출</button>
      </fieldset>
        <fieldset disabled>
          <legend>범례 2</legend>
            <div>
              <label for="fruitname">과일이름 : </label>
              <input type="text" name="fruit" id="fruitname">
            </div>
            <div>
              <label for="colorname">색 이름 : </label>
              <input type="text" name="color" id="colorname">
            </div>
          	<button type="submit">제출</button>
      </fieldset>
  </form>
  ```



- input type

  `text` / `password` / `email` / `tel`

  ```html
      <h3>Form</h3>
      <form action="" method="GET">
          <div>  
              <label> ID : 
                  <input type="text" name="id" minlength="6" maxlength="12">
              </label>
          </div>
          
          <div>     
              <label> PASSWORD : 
                  <input type="password" name="pwd">
              </label>
          </div>    
          
          <div>     
              <label> EMAIL : 
                  <input type="email" name="email">
              </label>
          </div>  
  
          <div>     
              <label> TEL : 
                  <input type="tel" name="tel">
              </label>
          </div> 
          <button type="submit">제출</button>
      </form>
  ```

  `number` / `range` / `date` / `month` / `time`

  ```html
      <h3>Form</h3>
      <form action="" method="GET">
          <div>  
              <label> NUMBER : 
                  <input type="number" name="number">
              </label>
          </div>
          
          <div>     
              <label> RANGE : 
                  <input type="range" name="range">
              </label>
          </div>
  
          <div>     
              <label> DATE : 
                  <input type="date" name="date">
              </label>
          </div>
  
          <div>     
              <label> MONTH : 
                  <input type="month" name="month">
              </label>
          </div>
  
          <div>     
              <label> TIME : 
                  <input type="time" name="time">
              </label>
          </div>
          
          <button type="submit">제출</button>
      </form>
  ```

  

  
  
  
  
  2021.09.03
  
  ------
  
  # 오늘의 정리
  
  
  
  **자주사용하는 input 속성**
  
  `submit` / `button` / `checkbox` / `radio`
  
  ```html
      <h3>Form</h3>
      <form action="" method="GET">
          <!-- submit기능을 기본으로 한다 -->
          <div> 
              <input type="submit" value="저장하기">
          </div>
          
          <!-- 형태를 보여주는 것으로 기능이 없음 -->
          <div>
              <input type="button" value="빈버튼">
          </div>
          
          <!-- 폼 내부에 있는 정보가 초기값으로 돌아간다 (초기화) -->
          <div>
              <input type="reset">
          </div>
          
          <!-- 중복선택x, 선택된 값이 url에 표시됨(on이 붙어서 표시됨) 
  		checked 값을 넣으면 기본으로 체크가 되어있음 -->
          <div>     
              <label> CHECKBOX : 
                  <input type="checkbox" name="check1" checked>
                  <input type="checkbox" name="check2">
                  <input type="checkbox" name="check3">
              </label>
          </div>
  
          <!-- 한가지만 선택이 가능, value를 넣으면 url에 표시됨
  		checked 값을 넣으면 기본으로 체크 -->
          <div>     
              <label> RADIO : 
                  <input type="radio" name="radio" value="r1">
                  <input type="radio" name="radio" value="r2" checked>
                  <input type="radio" name="radio" value="r3">
              </label>
          </div>
          
          <button type="submit">제출</button>
      </form>
  ```

- 

  `placeholder` : 예시로 보여주는 값

  `autocomplete` : 자동완성 기능, 기존에 입력한 내용을 사용할 수 있도록 보여줌

  `required` : 입력하지 않고 제출할 경우 비어있는 공간을 입력하도록 알림을 보여줌

  `disabled` : 비활성화, 값을 사용하지 않을 때(자바스크립트를 사용 할 때 주로 사용), 폼데이터에 포함되지 않음

  `readonly` : 읽기 전용. 포커싱은 되지만 입력은 되지 않음. 폼데이터에 포함(기본값을 포함)

  `min` : 최소값을 지정

  `max` : 최대값을 지정

  `step` : 숫자의 간격을 설정

  ```html
  <h3>Form</h3>
      <form action="" method="GET">
          
          <div>  
              <label for="username"> 이름 : </label>
              <input type="text" 
                     name="name" 
                     id="username" 
                     placeholder="홍길동" 
                     autocomplete="on"
                     required>
          </div>
          <div>  
              <label for="job"> 직업 : </label>
              <input type="text" 
                     name="job" 
                     id="job" 
                     placeholder="ex) 교사"
                     required>
          </div>
          <div>  
              <label for="age"> 나이 : </label>
              <input type="text" 
                     name="age" 
                     id="age" 
                     placeholder="29"
                     required
                     >
          </div>
          <div>  
              <label for="score"> 평점 : </label>
              <input type="numbur"
                     name="score"
                     id="score" 
                     min="-10"
                     max="10"
                     >
          </div>
          
          <input type="reset">
          <input type="submit">
      </form> 
          
  ```



- `<Button>`

  폼 내부의 제출하기, 리셋 등으로 사용 가능 input 타입과 동일하게 사용한다.

  input과 크게 차이점은 없지만 스타일을 적용하기가 수월하다.

  - type : `submit` / `reset` / `button`

    ```html
    <input type="reset" value="RESET">
    <input type="submit" value="제출하기">
    <input type="button" value="빈버튼">
    
    <button type="reset">RESET</button>
    <button type="submit">제출하기</button>
    <button type="button">빈버튼</button>
    ```



- `<select>` : 드롭다운 메뉴. 옵션 메뉴를 제공하는 컨트롤을 나타낸다

  `required`를 넣어서 옵션중에서 반드시 선택하여 제출

  하나의 옵션 값에 `selected`를 넣으면 새로고침을 했을때 해당 옵션에 고정된다

  `<optiongrorp label="">` 을 사용해서 장르(원하는 대로)를 묶어서 사용할 수도 있다.

  ```html
  <label for="movie">좋아하는 영화 : </label>
  
  	<select name="movie" id="movie-select" required>
          <!-- 후보군 메뉴 -->
          <option value="">--Please choose option--</option>
          <optiongrorp label="animation">
              <option value="toystory">토이스토리</option>
              <option value="zootopia">주토피아</option>
              <option value="rapunzel" selected>라푼젤</option>  
          </optiongrorp>
          <optiongrorp label="action">
              <option value="babydriver">베이비드라이버</option>
              <option value="ironman">아이언맨</option>
          </optiongrorp>
        </select>
  <input type="submit">
  ```

  ```
  https://developer.mozilla.org/ko/docs/Web/HTML/Element/select
  ```

  











