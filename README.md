# HTML
## HTML이란?
HTML(**H**yper**t**ext **M**arkup **L**anguage)은 마크업 언어로 웹 페이지의 구조, 의미 즉, 기본적인 형태를 만드는 코드이다.  
컨텐츠의 서로 다른 부분들을 씌우거나 감싸서 다른 형식으로 보이게하거나 특정한 방식으로 동작하도록 하는 일련의 요소로 이루어져있다.
  
## HTML 구조
![HTML 구조](https://blogfiles.pstatic.net/MjAyMTA5MTJfMTY4/MDAxNjMxNDI1MzM0NjE1.Zqp3D87NuuK_Knw1XIj112scin7uwjGmwv-f3JLH7OIg.RZQlnaQSvZ5BE7e0YxCyaNR0lbNcTCiyXmUyIkWYS84g.PNG.chlwnstjr94/image.png)
- Head : 각종 설정을 넣는 곳, CSS와 JavaScript를 연결
- Body : 화면의 요소들을 넣는 곳, 넣은 내용들이 사용자에게 보여짐
  
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
2. 속성 이름 뒤에는 **등호(=)**가 있어야한다.
3. 속성 값의 앞 뒤에 열고 닫는 **인용부호("또는')**가 있어야 한다.
  
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
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html>
```
|태그(tag)|설명|
|:--:|:--:|
|`<!DOCTYPE html>`|doctype은 HTML로 인정받기 위해 HTML 페이지가 따라야 할 규칙으로의 연결통로로써 작동하는 것을 의미하였다. 하지만, 최근에는 아무도 신경쓰지 않으며 그저 모든 것이 올바르게 동작하게 하기 위해 포함되어야 하라ㅏ 역사적인 유물일 뿐이다.
|`<html></html>`|페이지 전체의 컨텐츠를 감싸며 루트(root)요소라고도 한다.|
|`<head></head>`|HTML 페이지에 포함되어 있는 모든 것들의 컨테이너 역할을 한다. 검색 결과에 표시되길 원하는 페이지 설명, 컨텐츠를 꾸미기 위한 CSS, 문자 집합 선언 등과 같은 것들이 포함된다.|
|`<body></body>`|페이지에 방문한 모든 웹 사용자들에게 보여주길 원하는 모든 컨텐츠를 담고 있으며, 그것이 텍스트, 이미지, 비디오, 게임, 오디오 등 다른 무엇이든 될 수 있다.|
|`<meta charset="utf-8">`|문서가 사용해야 할 집합을 utf-8로 설정한다(utf-8 문자 집합에는 인간의 방대한 주류 기록언어에 있는 대부분의 문자가 포함되어 있다.). 사용할 수 있는 어떠한 문자 컨텐트도 다를 수 있다. 이 문자 집합을 설정하지 않을 이유가 없으며, 그렇게 설정하면 나중에 발생할 수 있는 일부 문제를 피할 수 있다.| 
|`<title></title>`|**페이지의 제목을 설정**하는 것으로 페이지가 로드되는 브라우저의 탭에 이 제목이 표시된다. 이 요소는 북마크나 즐겨찾기에서 페이지를 설명하는 것으로도 사용된다.|
  
### 이미지 태그 & 속성
```html
<img src="images/firfox-icon.png" alt="My test image">
```
|태그 & 속성|설명|
|:--:|:--:|
|`<img>`|이미지가 나타나야 할 위치에 이미지를 끼워 넣는다는 의미|
|`src(source)`|이미지 파일의 경로|
|`alt(alternative)`|설명문|
  
### 문자 태그
|태그|설명|
|:--:|:--:|
|`<h1~6></h1~6>`|제목 또는 하위 제목|
|`<p></p>`|문단|
|`<ul></ul>`|순서 없는 목록(블랙 포인트)|
|`<ol></ol>`|순서 있는 목록(숫자 목록)|
|`<li></li>`|목록 항목|
|`<a></a>`|링크 연결|