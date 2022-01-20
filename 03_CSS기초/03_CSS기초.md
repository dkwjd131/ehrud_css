# 1. 기본 선택자
* a : 지정된 모든 HTML a 태그
* .myClass : myClass 클래스가 적용된 모든 HTML 태그
* a.myClass : myClass 클래스가 적용된 HTML a 태그
* #myID : myID가 적용된 모든 HTML 태그
* a#myID : myID가 적용된 HTML a 태그
* \* : 모든 HTML 태그

<br><br>

# 2. 인라인 스타일
* 인라인 스타일은 스타일 적용시 우선순위가 가장 높다.
* HTML 태그에 직접 style 속성을 추가한다.
* ex) \<h1 style="color : red; font : italic bold;> ... \</h1>

<br><br>

# 3. 페이지 내 스타일
* 단일 웹 페이지에 적용할 스타일을 추가하려면 \<style> 태그를 사용한다.
* HTML 문서 어디에도 둘수 있지만 주로 \<head> 태그에 놓는게 좋다.
* ex)<br>
 \<style type="text/css", media = "all"><br>
 h1 {color: red;} <br>
\<style> <br>

<br><br>

# 4. 외부 스타일 [03_01_실습]
* 웹 사이트 전체에 스타일 시트를 적용하는 경우
* HTML 문서와 별도로 CSS 코드만 담고 있는 외부 CSS 파일
* CSS 파일에서 CSS 파일을 직접 링크하거나 불러올 수 있다.
* **다른 모든 CSS 코드보다 상단에 위치해야 한다.**

<br>

 
## 4.1 import로 불러오기

* HTML 문서 뿐 아니라 CSS 파일에서도 스타일 시트를 불어올 수 있다.
* HTML 문서의 \<head> ... \</head> 내에 \<style> 태그를 입력한다.  
    <br>
    EX) <br>
    *\<head> <br>
    \<style> <br>
    \@import{default.css} <br>
    *\@import url('default.css')* <br>
    \</style><br>
    \</head>* <br>
    <br>

## 4.2 **\<link> 태그로 연결하기**
* \<link> 태그를 사용하면 원하는 개수만큼 스타일 시트 파일을 링크할 수 있지만, 페이지 로딩이 느려질 수 있다.
* HTML 문서의 \<head> ... \</head> 내에 \<link> 태그를 입력한다. <br><br>
EX) <br>
*\<head> <br>
\<link <br>
rel : "stylesheet" <br>
href : "filename.css" <br>
type : "text/css" <br>
media = "all"\> <br>
\</head>* <br>

* **rel** : HTML 문서에 대한 링크 관계 입력. 다른 파일 타입을 추가하는 경우도 있다.
* **href** : CSS 문서의 전체 경로와 확장자를 포함한 이름 입력.
* **type** : 링크할 정보의 타입 입력. 예시는 CSS가 들어있는 텍스트 파일이다.
* **media** : 스타일 시트를 적용할 미디어 타입을 지정한다.

<br><br>

# 5. HTML 태그 CSS 정의
* 특정 HTML 태그를 사용한 모든 엘리먼트에 대해 CSS 선언을 할 수 있다.<br><br>

* 구문 <br>
*strong {color : gray}* <br>
HTML 문서에서 \<strong> 태그를 사용한 모든 엘리먼트에 회색 글씨 적용 <br><br>

* 선언 할 태그의 종류에 맞는 속성을 지정해야 한다. 예를 들어 인라인 엘리먼트인 \<b> 태그에는 text-indent 속성을 사용할 수 없다.

<br><br>

# 6. 클래스 선택자 CSS 정의
* 클래스에 해당하는 모든 태그에 적용 가능하다. <br>
<br>

## 6.1 클래스 선택자 
* 구문 <br>
*.className {font-size : 1em;}* <br>
클래스 이름이 className인 태그에 모두 적용

<br><br>

## 6.2 의존 클래스 선택자 
* 구문 <br>
*p.className {font-size : 1em;}* <br>
클래스 이름이 className인 \<p> 태그에만 적용

<br><br>

# 7. ID 선택자 CSS 정의
* ID는 HTML에서 페이지 레이아웃 구조를 구성하고 코드상의 고유 엘리먼트를 식별해 특정 엘리먼트를 별도 처리하는 데 사용한다. <br>

* CSS 나 자바스크립트에서의 위치 지정에 사용한다.

* **ID는 각 화면의 엘리먼트에 고유/식별성을 부여하기 때문에 페이지 당 한번만 ID를 사용하는 것이 적절하다.**
<br><br>

## 7.1 ID 선택자 
* 구문 <br>
*#idName {font-size : 1em;}* <br>
id 이름이 idName인 태그에 모두 적용

<br><br>

## 7.2 의존 ID 선택자 
* 구문 <br>
*p#idName {font-size : 1em;}* <br>
id 이름이 idName인 \<p> 태그에만 적용

<br><br>

# 8. 공통 선택자 CSS 정의
* 모든 HTML 선택자에 사용할 수 있다.
* 모든 자식 엘리먼트가 부모 엘리먼트의 스타일을 상속하는 것은 아니지만, 공통 선택자를 사용하면 모든 엘리먼트에 적용할 수 있다.

* 구문 <br>
**{font-size : 1em;}* <br>
모든 태그에 적용

<br><br>

# 9. 그룹 지정
* 동일한 스타일을 사용하는 선택자들을 동시에 선언할 수 있다. <br>

* 구문 <br>
*h1, h2, .copy, #head {font-size : 1em;}* <br>
h1, h2 HTML 선택자, .copy 클래스 선택자, #head id 선택자를 그룹화하여 동시에 적용

<br><br>

# 10. 스타일 시트의 주석
* 슬래시를 입력하고 별표를 입력하면 된다. <br>
* /* 주석 */