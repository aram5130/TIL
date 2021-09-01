2021.09.01

------

# 오늘의 정리



## 리스트 요소

### 목록

- Ordered List(순서가 있는 목록, 정렬)

  `<ol>` 0개 이상의 `<il>` 태그를 필요로 함.

  `<ol type="A">` type을 지정해서 사용 할 수 있다 / 1(기본값), A, a, I, i

  `<li>` 에 value 값을 넣어줄 경우 지정한 값으로 정렬됨.

  ```html
  <body>
      <ol>
          <li>바나나</li>
      	<li>딸기</li>
      	<li>복숭아</li>
      </ol>
  </body>
  ```

  

- Unodered List(순서가 없는 목록, 나열)

  `<ul>` 0개 이상의 `<il>` 태그를 필요로 함.

  중첩될 경우 불릿이 다르게 나타남.

  ```html
  <body>
      <ul>
          <li>바나나</li>
      	<li>딸기</li>
      	<li>복숭아</li>
      </ul>
  </body>
  ```



### 정의 목록

- 용어사전 구현이나 메타데이터(키-값 쌍 목록)를 표시할 때 사용

- `<dl>` 묶는 태그 / `<dt> ` 용어 / `<dd>` 정의

  ```html
  <dl>
      <dt>바나나</dt>
      <dd>바나나는 길쭉한 식용 과일로 무사 속의 여러 종류의 대형 초본 꽃 식물에 의해 생산됩니다.</dd>
  
      <dt>딸기</dt>
      <dt>strawberry</dt>
      <dd>딸기는 장미과 딸기속에 속하는 과일이다. 산딸기, 뱀딸기, 야생딸기 등과 재배하는 딸기로 구분된다. </dd>
  
      <dt>복숭아</dt>
      <dd>복숭아는 장미과 벚나무속에 속하는 복사나무의 열매이다. </dd>
      <dd>원산지는 중국 화북의 산시성과 간쑤성의 해발 600 ~ 2,000m 고원 지대이다.</dd>
  </dl>
  ```

### 표

- 행과 열로 이루어진 표

- `<table>` 

- `<tr> ` row 행 / `<th>` column 열 table head(열을 대표하는 내용) / `<td>` table data (단순한 내용)

- `<thead>` 테이블 태그의 바로 아래에 위치

- `<tbody>` 테이블 태그의 중간 부분

- `<tfoot>` 테이블 태그의 하단

  나누어서 만들어두면 css를 사용하기 용이함.

- `<caption>` 표 설명 요소, table요소 상단에 위치시켜야 함.

  (css로 위치 이동 가능.)

  ```html
  <table>
      <caption>나라별 인구</caption>
      <thead>
        <tr>
          <th>나라이름</th>
          <th>수도</th>
          <th>인구</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">한국</th>
          <td>서울</td>
          <td>5100만</td>
        </tr>
        <tr>
          <th scope="row">미국</th>
          <td>워싱턴DC</td>
          <td>3억</td>
        </tr>
        <tr>
          <th scope="row">태국</th>
          <td>방콕</td>
          <td>6900만</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td colspan="2">합계</td>
          <td>4억 2000만</td>
        </tr>
      </tfoot>
  </table>
  ```

