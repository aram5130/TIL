2021.08.31

------

# 오늘의 정리



## 텍스트 요소

### 본문

- Heading 제목 `<h1>`

  HTML의 제목을 표현하는 <h>태그 <h1>부터 <h6> 까지 다양한 사이즈를 사용

  ```html
  <body>
      <h1>제목 h1 입니다</h1>
      <h2>제목 h2 입니다</h2>
      <h3>제목 h3 입니다</h3>
      <h4>제목 h4 입니다</h4>
      <h5>제목 h5 입니다</h5>
      <h6>제목 h6 입니다</h6>
  </body>
  ```



- Paragraph 문단 `<p>` + 줄 바꿈 요소 `<br>`

  내용상 끊어서 구분할 수 있는 부분을 의미하고, 문단이라고도 함.

  ```html
  <body>
      <h1>제목 h1 입니다</h1>
      <p>본문입니다. 본문입니다.</p>
      <p>본문입니다.
      줄을 나눠도 하나의 단락으로 인식.</p>
      <p>가운데에 <br> 을 넣으면 줄바꿈!</p>
  </body>
  ```



- 인용 블록 요소 `<blockquote>` 와 인라인 인용문 `<q>` 

  ```html
  <body>
      <blockquote>안쪽의 텍스트가 긴 인용문임을 나타냅니다. 주로 들여쓰기를 한 것으로 보여짐
      용문의 출처 URL은 cite 특성으로, 출처 텍스트는 <cite> 요소로 제공할 수 있음.</blockquote>
      <q>둘러싼 텍스트가 짧은 인라인 인용문이라는것을 나타냄.
          대부분의 브라우저에서는 앞과 뒤에 따옴표를 붙여 출력됨. 줄바꿈이 없는 짧은 내용에 사용.</q>
  </body>
  ```



- Preformatted미리 서식 지정된 텍스트 `<pre>`

  HTML 파일에 기록된 텍스트와 모든 공백, 줄 나누기를 그대로 보여지게 함.

  ```html
  <body>
      <pre>
          L          TE
            A       A
              C    V
               R A
               DOU
               LOU
              REUSE
              QUE TU
      </pre>
  </body>
  ```



- figure  `<figure>`, `<figcaption>`

  독립적인 콘텐츠를 표현

  ```html
  <body>
      <p>첫번째 구분선</p>
      <hr>
      <p>두번째 구분선</p>
      <hr>
      <p>세번째 구분선</p>
      <hr>
  </body>
  ```

  

- Horizontsl rule 수평 가로 구분선 `<hr>`

  단란을 나눌 때, 내용상의 구분이 필요한 경우 사용.

  ```html
  <body>
      <p>첫번째 구분선</p>
      <hr>
      <p>두번째 구분선</p>
      <hr>
      <p>세번째 구분선</p>
      <hr>
  </body>
  ```



- 약어 표현 `<addr>` title과 함께 사용

-  주소 (지역, 이메일, SNS 등등) `<address>`

- 출처를 표기할 때 사용 `<cite>` 

- 현재 텍스트의 쓰기 방향을 덮어쓰고 다른 방향으로 렌더링 할 때 `<bdo>`

  ```html
  <body>
      <abbr title="World Wide Web">WWW</abbr>
      <address>
          <P>서울시 강동구 천호대로 0000</P>
          <a href="http://www.google.co.kr">google</a>
          <cite>출처는 여기, 제목을 포함해야한다.</cite>
          <p><bdo dir="rtl">텍스트를 반대 방향으로 작성할때</bdo></p>
      </address>
  </body>
  ```



### 포매팅

- **굵은 글씨** `<b>`, `<strong>`

  `<b>` : 시각적으로 굵게 보여지는 것을 원할 때 사용

  `<strong>` : 높은 중요도를 가지고 있는 경우 사용

  ```html
  <body>
      <P>글씨를 쓰다가 중요한 부분이 나올 경우에는<strong>이렇게 강조!</strong> 
         시각적으로 강조된 걸 원한다면 <b>이렇게 사용!</b></P>
  </body>
  ```

- *이탤릭체*  `<i>`, `<em>` 기울임꼴로 표현

   `<i>` : 주위와 구분해야하는 부분. ex) 기술용어, 외국어구절, 등장인물의 생각 등

  `<em>` : 텍스트의 강세를 나타냄

- 텍스트 강조 하이라이트 `<mark>`

  형광펜 효과, 브라우저별로 다르게 나타날수 있음.

- 덧붙임 요소 `<small>`

  덧붙이는 글이나, 저작권, 법률, copylight 들을 나타낼 때 사용

- 위/아래 첨자 `<sup>` / `<sub>`

  `<sup>` : 위 첨자, 글씨를 작게 만들어 위쪽으로 올림(제곱표시)

  `<sub>` : 아래 첨자. 각주를 나타내고 수식을 나타낼 때

- 제거된 텍스트 범위 (~~취소줄~~) `<del>`,
- 추가된 텍스트 범위 (텍스트 뒤로 bg) `<ins>`

### a 태그

```html
<body>
    <!-- 절대경로 -->
	<a href="http://www.google.co.kr">google</a>
    
    <!-- 상대경로 -->
	<a href="another/01.html">다른 파일</a>
    
    <!-- 상대경로 -->
	<a href="mailto:another@email.com">Send mail</a>   
    <a href="tel:123-4567">02) 123-4567</a>  
</body>
```

### Entity Code

| **엔티티 코드** | **문자식 표현(Entity Code)** | **숫자식 표현(Entity Number)** |
| --------------- | ---------------------------- | ------------------------------ |
| `<`             | `&lt;`                       | `&#8249;`                      |
| `>`             | `&gt;`                       | `&#8250;`                      |
| `©`             | `&copy;`                     | `&#169;`                       |
| `"`             | `&quot;`                     | `&#34;`                        |
| `&`             | `&amp;`                      | `&#38;`                        |
| `공백`          | `&nbsp;`                     | `&#160;`                       |



## 구조를 나타내는 요소

- 컨테이너

  `<div>` : 다른 요소들을 묶어 class / id 속성으로 꾸미지 위해 사용. 별도의 속성을 가지고 있지 않음. (블럭 요소)

  `<span>` : 인라인 컨테이너로 구문 콘텐츠를 담는다. 별도의 속성을 가지고 있지 않음. (인라인 요소)

- 시멘틱 웹 (Semantic Web)

  Semantic : 의미의, 의미론적인

  요소의 의미를 고려하여, 구조를 설계하고 코드를 작성한다.

  ```
  장점
  - 검색 랭킹에 영향을 줄 수 있다.
  - 스크린리더를 사용하는 사용자에게 의미론적 마크업을 사용할 수 있게 해줌.
  - 의미있는 코드 블록을 찾는 것이 용이.
  - 개발자에세 태그안에 채워질 데이터 유형을 제안.
  ```

- header / footer

  header : 소개 및 탐색에 도움을 주는 콘텐츠를 나타냄. 제목, 로고, 검색 폼, 작성자 이름 등의 요소도 포함할 수 있다.

  footer : 가장 가까운 구획 콘텐츠나 구획 루트의 푸터를 나타냄. 일반적으로 구획의 작성자, 저작권 정보, 관련 문서 등의 내용을 가짐.

  ```
  참고자료
  https://developer.mozilla.org/ko/docs/Web/HTML/Element/header
  https://developer.mozilla.org/ko/docs/Web/HTML/Element/footer
  ```

- nav (navigation)

  현재 페이지 내, 또는 다른 페이지(상하위)로의 링크를 보여줌

  탐색 구획 요소

```
참고자료
https://developer.mozilla.org/ko/docs/Web/HTML/Element/nav
```

- aside (side bar)

  주요 내용과 간접적으로 연관된 부분을 내타냄.

```
참고자료
https://developer.mozilla.org/ko/docs/Web/HTML/Element/aside
```

- main

  문서에서 하나만 존재.

```
참고자료
https://developer.mozilla.org/ko/docs/Web/HTML/Element/main
```

- article

  사이트 안에서 독립저으로 구분해 배포하거나 재사용할수 있는 구획

  ex) 게시판 / 블로그 글 / 매거진 등

  <h1*></h*1> 제목 요소를 <article> 의 자식으로 포함하는 방법을 사용.

```
참고자료
https://developer.mozilla.org/ko/docs/Web/HTML/Element/article
```

- section

  단독적으로 사용이 불가능, article안에 위치해 있음.

  <h1*></h*1> 제목 요소를 <article> 의 자식으로 포함하는 방법을 사용 할 수 있음.

  일반 컨테이너로 사용하지 않음.

  ```
  참고자료
  https://developer.mozilla.org/ko/docs/Web/HTML/Element/section
  ```

  
