# HTML
## HTML이란?
HTML(**H**yper**t**ext **M**arkup **L**anguage)은 마크업 언어로 웹 페이지의 구조, 의미 즉, **기본적인 형태**를 만드는 코드이다.  
컨텐츠의 서로 다른 부분들을 씌우거나 감싸서 다른 형식으로 보이게하거나 특정한 방식으로 동작하도록 하는 일련의 요소로 이루어져있다.
  
## HTML 구조
![HTML 구조](https://blogfiles.pstatic.net/MjAyMTA5MTJfMTY4/MDAxNjMxNDI1MzM0NjE1.Zqp3D87NuuK_Knw1XIj112scin7uwjGmwv-f3JLH7OIg.RZQlnaQSvZ5BE7e0YxCyaNR0lbNcTCiyXmUyIkWYS84g.PNG.chlwnstjr94/image.png)
- Head : 사용자에게 보여지는 요소는 없고 브라우저에서 검색할 때 나오는 타이틀이나 부가설명 그리고 북마크 추가할때 나오는 제목이나 아이콘들 등이 정의된다, CSS와 JavaScript 파일를 연결  

- Body : 화면의 요소들을 넣는 곳, 넣은 내용들이 사용자에게 보여지는 가장 중요한 최상의 컨테이너이다.  
  body안에는 작성한 내용들이 바로 사용자한테 보여지는 태그들로 이루어져 있다.
  
## HTML 요소 분석
![HTML 요소](https://mdn.mozillademos.org/files/9347/grumpy-cat-small.png)
1. opening tag(여는 태그) : 요소의 이름으로 구성되고, <>로 감싸진다. 이것은 **요소가 시작되는 곳**, 또는 **효과를 시작하는 곳**임을 나타낸다.
2. closing tag(닫는 태그) : 요소의 이름 앞에 /가 포함된다는것이 여는 태그와의 차이점이다. **요소의 끝**을 나타낸다.
3. content(컨텐츠) : **요소의 내용**이다.
4. element(요소) : **여는 태그, 닫는 태그 그리고 컨텐츠**로 이루어져있다.
  
## HTML 속성
![HTML 속성](https://mdn.mozillademos.org/files/9345/grumpy-cat-attribute-small.png)
**추가적인 정보**를 담고 있다. 해당 요소를 특정해 스타일이나 다른 정보를 설정할 때 사용할 수 있는 식별자를 지정할 수 있다.
#### 속성이 가져야 하는 것
1. 요소 이름과 속성 사이의 **공백**이 있어야한다.
2. 속성 이름 뒤에는 **등호**(=)가 있어야한다.  
  (등호는 "오른쪽에서 왼쪽으로 적용시킨다"는 뜻이다.)
3. 속성 값의 앞 뒤에 열고 닫는 **인용부호**("또는')가 있어야 한다.
  
## 요소 중첩
요소를 다른 요소의 안에 놓을 수 있다. 이것을 중첩(nesting)이라고 한다.
> 예시 : 우리집 강아지는 **아주** 착해
```html
<p>우리집 강아지는 <strong>아주</strong> 착해.</p>
``` 
위의 예시 처럼 요소들이 적절히 열고 닫혀야 서로가 깔끔하게 안쪽이나 바깥쪽에 있게 된다.
  
## 빈 요소
어떤 요소들은 내용을 가지고 있지 않는다. 이것을 빈요소(empty elements)라 한다.
`<img>`요소가 이에 해당한다.
```html
<img src="images/firfox-icon.png" alt="My test image">
```
`<img>`요소는 두 개의 속성을 포함하고 있으나 닫는 태그(`</img>`)가 없다.  
이미지 요소는 효과를 주기 위해 컨텐츠를 감싸지 않기 때문이다.  
이 요소의 목적은 HTML 페이지에서 이미지가 나타날 위치에 이미지를 끼워 넣는 것이다.
  
---
## HTML 태그(tag)
### 기본 구조 태그
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html>
```
|태그(tag)|설명|
|:--:|:--:|
|`<!DOCTYPE html>`|doctype은 HTML로 인정받기 위해 HTML 페이지가 따라야 할 규칙으로의 연결통로로써 작동하는 것을 의미하였다. html5버전을 나타낸다.|
|`<html></html>`|페이지 전체의 컨텐츠를 감싸며 루트(root)요소라고도 한다.|
|`<head></head>`|HTML 페이지에 포함되어 있는 모든 것들의 컨테이너 역할을 한다. 검색 결과에 표시되길 원하는 페이지 설명, 컨텐츠를 꾸미기 위한 CSS, 문자 집합 선언 등과 같은 것들이 포함된다.|
|`<meta charset="utf-8">`|문서가 사용해야 할 글자의 포맷을 utf-8로 설정한다(utf-8 문자 집합에는 인간의 방대한 주류 기록언어에 있는 대부분의 문자가 포함되어 있다.). 사용할 수 있는 어떠한 문자 컨텐트도 다를 수 있다.| 
|`<meta name="viewport" content="width=device-width">`|디바이스 스크린의 너비를 전부 사용한다고 정의
|`<title></title>`|**페이지의 제목을 설정**하는 것으로 페이지가 로드되는 브라우저의 탭에 이 제목이 표시된다. 이 요소는 북마크나 즐겨찾기에서 페이지를 설명하는 것으로도 사용된다.|
|`<body></body>`|페이지에 방문한 모든 웹 사용자들에게 보여주길 원하는 모든 컨텐츠를 담고 있으며, 그것이 텍스트, 이미지, 비디오, 게임, 오디오 등 다른 무엇이든 될 수 있다.|
  
### 이미지 태그 & 속성
어떤 요소들은 내용을 가지고 있지 않는다. 이것을 빈요소(empty elements)라 한다. <img>요소가 이에 해당한다.
```html
<img src="images/firfox-icon.png" alt="My test image">
```
> `<img>` : 이미지가 나타나야 할 위치에 이미지를 끼워 넣는다는 의미
  
|속성|설명|
|:--:|:--:|
|`src(source)`|이미지 파일의 경로|
|`alt(alternative)`|설명문|  
|`width`|이미지의 픽셀 기준 고유 너비, 단위 없는 정수 사용|
|`height`|이미지의 고유 크기, 단위 없는 정수 사용|
  
`<img>`요소는 두 개의 속성을 포함하고 있으나 닫는 태그(`</img>`)가 없다.  
이미지 요소는 효과를 주기 위해 컨텐츠를 감싸지 않기 때문이다.  
이 요소의 목적은 HTML 페이지에서 이미지가 나타날 위치에 이미지를 끼워 넣는 것이다.
  
### 비디오 태그 & 속성
> `<video>`: 비디오가 나타나야 할 위치에 비디오를 끼워 넣는다는 의미
  
|속성|설명|
|:--:|:--:|
|`src(source)`|비디오 파일의 경로|
|`controls`|비디오 재생버튼, 소리 조절을 할 수 있는 컨트롤러 활성|
|`width`|비디오의 출력 영역 너비|
|`height`|비디오의 출력 영역 높이|
  
### 오디오 태그 & 속성
> `<audio>`: 문서에 소리 콘텐츠를 포함할 때 사용
  
|속성|설명|
|:--:|:--:|
|`src(source)`|오디오 파일의 경로|
|`controls`|오디오 재생버튼, 소리 조절을 할 수 있는 컨트롤러 활성|
  
### 텍스트 태그
|태그|설명|
|:--:|:--:|
|`<h1~6></h1~6>`|제목 또는 하위 제목|
|`<b></b>`|굵은 글씨|
|`<i></i>`|기울은 글씨|
|`<p></p>`|문단|
|`<span></span>`|구문 콘텐츠를 위한 통용 인라인 컨테이너, 서로 공유하는 요소를 묶을 때 사용|
|`<br>`|줄바꿈, 줄의 구분이 중요한 내용을 작성할 때 유용|
  
### 목록 태그
|태그|설명|
|:--:|:--:|
|`<ul></ul>`|순서 없는 목록(블랙 포인트)|
|`<ol></ol>`|순서 있는 목록(숫자 목록)|
|`<li></li>`|목록 항목|
  
### 링크 태그 & 속성
> `<a></a>` : 링크 연결
  
|속성|설명|
|:--:|:--:|
|`href`|하이퍼 텍스트 참조(**h**ypertext **ref**erence) 속성|
|`rel`|연결한 URL과의 관계를 나타냄|
|`target`|링크한 URL을 표시할 위치|
|`target_blank`|URL을 새로운 브라우징 맥락에 표시|
|`target_self`|URL을 현재 브라우징 맥락에 표시|
  
### form 태그 & 속성
> `<form></form>`: 정보 제출을 위한 대화형 컨트롤을 포함하는 문서 구역
  
|속성|설명|
|:--:|:--:|
|`target`|양식 제출 결과를 표시할 위치|
|`target_blank`|응답을 새로운 브라우징 맥락에 표시|
|`target_self`|응답을 현재 브라우징 맥락에 표시|
  
### input 태그 & 속성
> `<input></input>`: 사용자의 데이터를 받을 수 있는 대화형 컨트롤을 생성
  
|속성|설명|
|:--:|:--:|
|`type`|type 특성에 따라 input의 요소 동작 방식이 달라진다.|
  
### label 태그 & 속성
> `<label></label>`: 인터페이스 항목의 설명
  
|속성|설명|
|:--:|:--:|
|`for`|레이블 가능한 요소의 id. 레이블 가능한 요소일 때, for 속성값과 일치하는 id를 가진 문서의 첫 번째 요소는 그 label 요소의 라벨 제어라고 합니다. label을 지정할 수 없으면 for 속성은 영향을 미치지 않습니다. 문서의 뒷부분에 id 값과 일치하는 다른 요소들은 무시합니다.|
  
### 버튼 태그 & 속성
> `<button></button>`: 클릭 가능한 버튼을 나타낸다.
  
|속성|설명|
|:--:|:--:|
|`name`|버튼 이름|
|`type`|버튼의 행동 방식|
  
### iframe 태그 & 속성
> `<iframe></iframe>`: 중첩 브라우징 맥락을 나타내는 요소, 현재 문서 안에 다른 HTML 페이지를 삽입
  
|속성|설명|
|:--:|:--:|
|`src`|페이지의 URL의 경로|
|`width`|프레임의 너비|
|`height`|프레임의 높이|
  
## Semantics
프로그래밍에서 **시맨틱**은 *코드 조각의 의미*를 나타낸다.
  
## HTML Semantics(시맨틱)
HTML은 채워질 데이터를 나타내도록 코딩해야한다.
  
### 의미론적 마크업을 사용 시 이점
* 검색 엔진은 의미론적 마크업 을 페이지의 검색 랭킹에 영향을 줄 수 있는 중요한 키워드로 간주한다.
* 시각 장애가 있는 사용자가 화면 판독기로 페이지를 탐색할 때 의미론적 마크업을 푯말로 사용할 수 있다.
* 의미없고 클래스 이름이 붙여져있거나 그렇지 않은 끊임없는 `div` 들을 탐색하는 것보다, 의미있는 코드 블록을 찾는 것이 훨씬 쉽다.
* 개발자에게 태그 안에 채워질 데이터 유형을 제안한다.
* 의미있는 이름짓기(Semantic naming)는 적절한 사용자 정의 요소 / 구성 요소의 이름짓기(namimg)를 반영한다.
  
## 의미론적 요소(element)
### `<header>`
* **소개 및 탐색에 도움**을 주는 콘텐츠를 나타낸다.
* 제목, 로고, 검색 폼, 작성자 이름 등의 요소를 포함할 수 있다.
  
### `<footer>`
* 가장 가까운 구획 콘텐츠나 구획 루트의 푸터를 나타낸다.
* 일반적으로 **구획의 작성자, 저작권 정보, 관련 문서** 등의 내용을 담는다.
  
### `<nav>`
* 문서의 네비게이션 항목을 정의, 컨텐츠를 탐색할 때 사용하는 정보를 알려준다.
  
### `<article>`
* **본문**에 사용한다.
* 문서, 페이지, 애플리케이션, 또는 사이트 안에서 독립적으로 구분해 배포하거나 재사용할 수 있는 구획을 나타낸다.  
* 사용 예제로 게시판, 블로그 글, 잡지, 뉴스 기사 등이 있다.
* 하나의 문서에 여러 개의 `<article>`을 가질 수 있다.
  
### `<section>`
* 문서들의 구역들을 정의
* 서로 다른 영역을 구분하기 위해 사용
* section안에 article이 있다.
  
### `<main>`
* 문서에서 가장 중심이 되는 컨텐츠를 정의

### `<aside>`
* 광고와 같이 문서의 주요 내용과 연관이 적은 부분을 나타낸다.
* 주로 사이드바 혹은 콜아웃 박스로 표현한다.
  
### `<details>`
* 기본적으로 화면에 표시되지 않는 정보들을 정의
  
### `<figure>`
* 삽화와 같은 부가적인 요소를 정의
  
### `<mark>`
* 참조, 하이라이트 표시를 필요로하는 문자를 정의
  
### `<time>`
* 시간을 정의
  
## 에밋(emmet)
-  HTML, XML, XSL 문서 등을 편집할 때 빠르고 쉽게 코딩을 작성하기 위해 사용
- 매우 간단한 몇 가지 코드만 입력하면, 자동으로 완전한 HTML 코드를 생성해 준다.
  
### 방법
- !을 입력 후 tab을 누르면 기본적인 html구조 작성
- div는 생략가능, 나머지 태그는 입력해야함
- #=id, .=class, *=곱하기를 나타낸다.
