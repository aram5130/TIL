2021.08.30

------

# 오늘의 정리



## HTML

### 하이퍼 텍스트 마크업 언어(Hyper Text Markup Language, HTML)

HTML은 제목, 단락, 목록 등과 같은 본문을 위한 구조적 의미를 나타내는 것뿐만 아니라 링크, 인용과 그 밖의 항목으로 구조적 문서를 만들 수 있는 방법을 제공한다

- 마크업 언어 : 데이터를 그 자체로 어떤 역할을 가지고 있고 보여지는지 구조를 정의

- 프로그래밍 언어 : 데이터를 가공해서 어떻게 해야한다- action

  

```
참고자료
1. https://ko.wikipedia.org/wiki/HTML
2. https://developer.mozilla.org/ko/docs/Web/HTML
```





### HTML / CSS / JavaScript

```
- [구조] HTML : 웹 문서의 기본적인 골격을 담당.
- [표현] CSS : 각 요소들의 레이아웃, 스타일링을 담당.
- [동작] JavaScript : 동적인 요소(사용자와의 인터랙션)을 담당. 
```



### 웹 표준 / 웹 접근성 / 웹 호환성

- 웹 표준 (Web Standards) : W3C에서 HTML5를 14년도에 공식 표준화

  웹 사이트나 웹 페이지가 웹 표준을 준수한다는 것은 일반적으로 올바른 HTML, CSS, 자바스크립트를 사이트나 페이지가 가지고 있다는 것

- 웹 접근성 (Web Accessibility) : 웹 접근성은 웹 사이트, 도구, 기술이 장애를 가진 사용자들이 사용할 수 있도록 설계 및 개발된 것

- 웹 호환성 (Cross Browsing) :  웹 브라우저 버전, 종류와 관계없이 웹사이트 접근

  HTML, CSS 문법 준수 / 동작, 레이아웃, 플러그인 호환성






## 메타데이터 요소

### 메타데이터

- 데이터를 설명하는 데이터 (데이터를 위한 데이터)

  문서의 정보를 분류하는 것

  

  ###### title : 브라우저의 제목 표시줄 or 페이지 탭에 보이는 요소

  ###### meta : 

  ###### 			- 문자 인코딩(charset="UTF-8"), 

  ###### 			- 문자 뷰포트(name="viewport") : 모바일 장치에서 사용

  ```
  참고자료
  https://developer.mozilla.org/ko/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML
  ```

  

  ###### mime Type : 외부에 있는 파일을 불러와서 경로를 지정할 때, 

  ###### 						경로를 해석 할 수 있도록 하기위해 사용하는 것

  ```
  참고자료
  https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP/MIME_types
  ```

  

  ###### style : css문법을 사용해서 스타일을 적용

  ```
  참고자료
  https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/style
  ```

  

  ###### script : 데이터와 실행 가능한 코드를 문서에 포함할 때 사용하며 보통 JavaScript 코드와 함께 사용

  ```
  참고자료
  https://developer.mozilla.org/ko/docs/Web/HTML/Element/script
  ```

  