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

  text / password / email / tel

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

  number / range / date / month / time

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

  **자주사용하는 input 속성**

  

















