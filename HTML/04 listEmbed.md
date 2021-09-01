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



## 임베디드 요소

### 외부의 소스를 불러와서 삽입하는 것

- `<img>`이미지 태그

  닫는 태그가 없이 내부에 내용(소스)를 넣어서 사용

  - src 특성은 필수, 포함하고자 하는 이미지의 경로를 지정 (절대경로, 상대경로)

  ```html
  <body>
      <!-- 절대 경로 -->
      <img src="https://cdn.pixabay.com/photo/2021/08/24/15/38/sand-6570980__340.jpg"
           alt="흑백모래사진">
      <!-- 상대 경로 -->  
      <img src="image/01.jpg">
  </body>
  ```

  - alt(Alternate) 대체 텍스트 속성

    접근성을 높혀주는 속성, 네트워크 오류, 콘텐츠 차단 등의 문제로 이미지가 나오지 않을 경우 사용.

  

  - width / height 속성 : 숫자를 속성의 값으로 받는다.

    width 가로 길이

    height 높이 길이

- 웹에서 사용하는 이미지 유형

  래스터 이미지 `JPEG` `PNG` `GIF` `WEBP` : 배경이나 사진

  백터 이미지 `SVG` : 아이콘이나 그래프, UI 요소에 사용

  | abbreviation | MIME type       | File extension(s)                      | Summary                                                      |
  | ------------ | --------------- | -------------------------------------- | ------------------------------------------------------------ |
  | JPEG         | `image/jpeg`    | `.jpg` `.jpeg` `.jfif` `.pjpeg` `.pjp` | 정지 이미지의 손실 압축에 적합 (현재 가장 많이 사용)         |
  | PNG          | `image/png`     | `.png`                                 | PNG는 원본 이미지를 보다 정확하게 보여주거나 **투명도**가 필요한 경우 JPEG보다 선호 |
  | GIF          | `image/gif`     | `.gif`                                 | 여러장의 이미지로 이루어진 애니메이션 표현                   |
  | WEBP         | `image/webp`    | `.webp`                                | 구글이 만든 이미지 포맷, 품질, 압축률 등이 우수하지만 지원 브라우저가 제한적 |
  | SVG          | `image/svg+xml` | `.svg`                                 | 다양한 크기로 정확하게 그려야 하는 아이콘, 다이어그램 등에 사용 |




### 반응형 이미지

### Image

- srcset(viewport에 따라서 변경, 반응형)

  사용자 에이전트가 사용할 수 있는 이미지 소스의 후보, 쉼표로 구분하는 한개 이상의 문자열 목록

  1. 이미지의 URL

  2. 선택적으로, 공백을 넣고 너비 서술자와 픽셀 밀도 서술자를 넣는다.

     ```html
     <img
          src="image/large.png"
          srcset="image/small.png 300W,
     			image/medium.png 450W,
                  image/large.png 600W,"
          alt="responsive images"
      />
     ```

- sizes

  소스 크기를 나타내는, 쉼표로 구분한 하나 이상의 문자열. (고정)

  1. 미디어 조건. 마지막 항목에서는 생략

  2. 소스 크기의 값 min-width / max-width

     ```html
     <img
          src="image/large.png"
          srcset="image/small.png 300W,
     			image/medium.png 450W,
                  image/large.png 600W,"
          sizes="(min-width: 600px) 600px,
                 (min-width: 450px) 450px,
                 300px"
          alt="responsive images"
      />
     ```

### Video

- `<video>` `</video>` 비디오 태그는 이미지 태그와 다르게 닫는 태그가 존재함

  태그 내부에 autoplay 를 추가하면 자동으로 재생 가능함(갑자기 소리가 나는 것을 방지하기 위해 muted 속성을 함께 사용)

  태그 내부에 controls 를 추가하여, 재생바와 소리 조절등이 가능함

  poster 속성을 사용하면 썸네일 이미지를 사용 할 수 있음.

  ```html
  <videc src="video/20210901.mp4">
      Sorry, your browser doesn't support embedded videos.
  </videc>
  
  <videc>
      <source src="video/20210901.mp4">
      Sorry, your browser doesn't support embedded videos.
  </videc>
  ```



### Audio

- `<audio>` `</audio>` 비디오와 비슷한 속성을 사용함.

  figure 속성을 사용하고 controls 패널을 추가하여 하나의 묶음으로 사용할 수 있도록 하는 것을 추천

  ```html
  <figure>
      <figcaption>Listen to the T-Rex:</figcaption>
      <audio
          controls
          src="/media/cc0-audio/t-rex-roar.mp3">
              Your browser does not support the
              <code>audio</code> element.
      </audio>
  </figure>
  ```



