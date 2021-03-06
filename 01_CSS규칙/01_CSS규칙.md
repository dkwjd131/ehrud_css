# 1. CSS 규칙
* CSS 규칙은 HTML이 어떻게 보이고 브라우저 창에서 HTML이 어떻게 동작해야 하는지 정의한다.
* CSS 규칙에는 세 가지 종류가 있으며 각 규칙에는 고유한 용도가 있다.

<br><br>

# 2. CSS 규칙 종류
## 2.1 HTML 선택자
* HTML 태그 \<h1>에서 h1은 태그에 대한 선택자이다.
* HTML 선택자는 CSS 규칙에서 태그가 보이는 방식을 재정의 한다.
* 예를 들어 h1 {color: red;} 는 \<h1>에 스타일을 적용한다.

<br>

## 2.2 클래스 
* 클래스는 여러 HTML 태그에 모두 적용할 수 있다.
* 예를 들어 .myclass {font: bold 1.25em times;} 는 \<h1 class="myclass"> 에 스타일을 적용한다.

<br>

## 2.3 ID
* 클래스와 비슷하게 모든 HTML 태그에 적용할 수 있다.
* ID는 자바스크립트 함수에서 객체를 사용할 수 있도록 특정 페이지에서 특정 HTML 태그에 한 번만 적용해야 한다.
* 예를 들어 #myobject {position: absolute; ...} 는 \<h1 id="myobject"> 에 적용한다.

<br><br>

# 3. CSS 규칙 구성 요소
## 3.1 선택자
* HTML 태그 선택자
* 클래스 선택자
* ID 선택자
* 공통 선택자

<br>

## 3.2 속성
* 정의하는 내용을 나타낸다.
* 속성에는 수십가지가 있다.

<br>

## 3.3 값
* 속성에 대입해 속성의 성질을 나타낸다.
* 값의 종류는 속성에 전적으로 의존한다.

<br><br>

# 4. CSS 규칙 구문
* 예시) selector {property: value;}
* 위 예시에서 selector를 선택자(HTML, 클래스, ID), property를 속성, value를 값이라고 한다. 
* 속성과 값들을 나열한 중괄호{} 내용을 선언 부분이라고 한다. 세미콜론으로 구분하면 원하는 개수만큼 정의를 추가할 수 있다.