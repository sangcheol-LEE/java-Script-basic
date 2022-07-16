# HTML,CSS 첫걸음

## HTML

- 구조를 만드는 언어
- 마크업 언어

## CSS

- 웹의 시각적인 표현을 담당
- 예쁘게 만들어 주는 언어

## JS

- 콘텐츠를 바꾸고 움직이는 등 페이지를 동적으로 꾸며주는 역할을 하는 프로그래밍 언어로 웹의 동적 처리를 담당

## 웹 표준

- W3C의 권고안에서 나온 기술이고, 웹에서 사용되는 표준 기술이나 규칙 (HTML, CSS, JS)을 기반으로 웹 브라우저를 만듭니다.

## 크로스 브라우징

- 많은 브라우저들에서 동일한 결과물로 출력되게 만들어야 한다.

## 웹 접근성

- 누구나 쉽게 웹사이트를 이용할 수 있게 해주는 것
- 청각장애인을 위해 영상자막, 마우스를 사용할 수 없는 분들을 위해 키보드를 통해 웹사이트 사용, 이미지에 대체 텍스트 등

## 이미지에 대한 이해

- 비트맵과 벡터 이미지

* 비트맵

- 각 픽셀이 모여 만들어진 정보의 집합으로 레스터(Raster)이미지라고도 부릅니다.
- 픽셀 단위로 화면에 렌더링
- .JPG(.jpeg), .PNG, .gif 등

* 벡터

- 수학적 정보의 형태들이 만들어내는 결과물입니다.
- 이미지가 가지고 있는 점, 선, 면의 위치(좌표) 색상 등의 정보를 온전히 가지고 화면에 렌더링합니다.
- 확대 및 축소를 해도 이미지가 깨지지 않습니다.
- .svg

# HTML 기본문법

## 기본 형태

- 태그는 각자의 의미를 가지고 있으며 다음과 같은 형태를 가집니다.
- "<TAG></TAG>, <TAG>something</TAG>"

## 속성(Attributes)과 값 (value)

- 태그(요소)의 기능을 확장하기 위해 '속성'을 사용할 수 있습니다.
- <img src="imageUrl(이미지 경로)" alt=" 대체 텍스트 " />

## 부모와 자식요소

- "<parents> <Child></Child> <parents>"

## 빈 태그

- HTML에는 닫히는 개념이 없는 태그들이 있다.
- "<TAG />"
- "ex) <img />"
- html5 에서는 위 2가지 형태를 다 사용할 수 있는데 개발하는 환경에 따라 사용할 수 있는데 쓸꺼면 전부 다쓰고 안쓸꺼면 아예 쓰지말자
- 혼용만 하지말자 !

## HTML 문서의 범위

- DOCTYPE (DTD, Document Type Definition)은 마크업 언어에서 문서 형식을 정의합니다.
- <!DOCTYPE html>
- <html> 
      <head>
        문서의 정보 
      </head>
      <body>
        문서의 구조
      </body>
  </html>

## HTML 문서의 정보

- head 태그 안에서 사용되는 태그들은 문서의 정보를 가지고 있다.

1. title - 웹 페이지의 제목
2. meta - 웹 페이지의 정보 (웹 페이지에 관한 정보(표시 방식, 제작자, 내용, 키워드 등)를 검색엔진이나 브라우저에 제공, 빈 태그입니다.)
3. Link - 외부 문서를 연결할 때 사용합니다.
4. Style - css를 직접 작성하는 태그(css를 외부 문서에서 작성하여 연결하는 것이 아니라 html 문서 내부에서 작성할 때 사용)
5. Script - js 불러오거나 작성하기

- body 태그 안에서 사용되는 태그들읜 문서의 구조를 나타내고 화면에 직접 출력되는 태그들이다.

1. Div - 막 쓰는 태그
2. IMG - 이미지를 넣는 태그

# CSS

## 태그의 직접 작성하기 - 인라인 선언 방식

- <div style="color: red;"> 태그의 직접 작성 </div> 
  // 이 방법은 html 태그에 직접 작성하기 때문에 선택자가 필요하지 않습니다.
  // 자바스크립트가 html에 css를 강제삽입 할 때 사용하긴한다.

## HTML에 포함하기 - 내장 선언방식

- <head>
  <style> 
    div {
      color :red;
    }
  </style>
  </head>
  <body> 
    <div> html에 포함 </div>
  </body>

## HTML 외부에서 불러오기

- css 코드를 완전히 분리할 수 있습니다.
- 분리된 하나의 css 파일을 여러 html 파일이 불러와서 사용가능
- <link rel="stylesheet" href="./css/main.css">
- 경로 "./" => 내 주변에서 찾겠다.

## 선택자

- 선택자는 HTML의 특정한 요소를 선택하는 사인(Sign)입니다.

1. 태그로 찾기

- 선택자를 입력하는 부분에 적용하려는 태그의 이름을 입력
- h1 {
  color: red
  }
- p {
  color : blue
  }

- 클래스로 찾기 // class="title"은 글자색이 빨강색이야!
- .title {
  color: red;
  }

## 속성

- 크기,여백,색상 같은 눈에 보이는 스타일을 지정할 수 있다.

1. 크기

- width - 요소의 가로 너비
- height - 요소의 세로 너비
- font-size - 글자 크기

2. 여백

- margin - 요소의 바깥 여백
- padding - 요소의 내부 여백

3. 색상

- font-color - 요소의 글자 색상
- background-color - 요소의 배경 색상

# CSS

## 작업 전 초기화를 해줘야 한다.

## width 와 height의 기본 값은 auto로 되어있다.

- auto의 의미는 가로 사이즈는 100%로 꽉 차게 되고, height는 자식요소로 있는 요소들의 길이로 자동으로 늘어난다.

## margin auto

- margin은 요소의 바깥여백인데 부모의 width 값 기준으로 화면의 중앙으로 오게 된다.

## 블록요소와 인라인 요소

### 블록 div, h1, p 등

- 사용 가능한 최대 가로 너비를 사용
- 크기를 지정할 수 있다.
- width값이 100%로 시작, 높이는 없는 상태로 시작 (height: 0)
- 수직으로 쌓임
- margin,padding 위,아래,좌,우 사용 가능
- 레이아웃을 위한 용도

### 인라인span, img 등

- 필요한 만큼의 너비만 사용
- 크기를 지정할 수 없다.
- width: 0, height: 0 으로 시작
- 수평으로 쌓임
- margin,padding 위,아래 사용 불가
- 텍스트를 다루는 용도

## form

- autocomplete - 자동완성 기능 사용할지 말지 값 : on / off
- get 방식 : 정보들을 전송하려고 하는 url에 담아서 보내는 방식
- post 방식 : 그 정보가 url에 담긴 정보가 아니지만 특정한 보안을 해서 전송을 한다.

## input

- autofocus : 자동으로 포커스
- name : 양식의 이름 서버로 데이터를 보낼 때 해당하는 데이터가 어떤 이름을 가진지 정함
- type : 입력 받을 데이터의 종류

# CSS 실습

## css Reset

- 왜 css를 초기화 해야하는가 ?
- 브라우저가 가지고 있는 기본 css를 초기화 하여 크로스 브라우징을 해결 할 수 있도록 하기위함

## css 선택자

- 일치 선택자 span.className {} 둘 다 만족해야만 선택됩니다.
- 자식 선택자 ul > .className {}
- 후손(자손) 하위 선택자 div .className {}
- 인접 형제 선택자 .className + li {}
- 일반 형제 선택자 .className ~ li {}

## 가상 클래스 선택자

- :(콜론) 1개
- hover : 요소에 마우스 포인터가 올라가 있는 동안에만 동작 .className:hover {}
- active : 요소를 마우스로 클릭하는 동안에만 동작 .clasName:active {}
- focus : 요소에 포커스 된 동안에만 선택 (대화형 콘텐츠 input, img, tabindex 에 사용)
  .className:focus

## 가상 요소 선택자

- 가상의 요소에는 이미지도 넣을 수 있다.
- before : 요소 내부의 앞에 내용 (contant)을 삽입 (가상의 요소로 삽입)
- :: (콜론 2개) .className::before {}
- 예) div::before
- "<div> <가상요소 들어올 위치> 내용 </div>"

- ul li ::before {
  content : '숫자';
  font-weight: bold;
  }
- 어떤 특정한 요소에 특정한 값을 넣고싶을 때 사용합니다.

- after : 요소 내부의 뒤에 내용을 삽입
- ul li ::after {
  content : url("이미지주소");
  }

## CSS 상속

- 상속되는 속성들

* font

- font-size
- font-weight
- font-style
- line-height
- font-family

* color
* text-align
* text-indent
* text-decoration
* letter-spacing
* opacity ...

### 강제 상속 (필요에 의해서)

- 부모요소에 position : absolute 를 주면 상속되지 않는데 자식 요소에 position : inherit을 주면 부모요소의 값을 강제로 상속받아 사용 할 수 있다.

## 우선순위

- 같은 요소가 여러 선언의 대상이 될 경우, 어떤 선언의 css속성을 우선 적용할지 결정하는 방법

1. 명시도 점수가 높은 선언이 우선 명시도
2. 점수가 같은 경우, 가장 마지막에 해석(늦게 작성한) 되는 선언이 우선 (선언순서)
3. 명시도는 "상속" 규칙보다도 우선
4. !important 가 적용된 선언방식이 다른 모든 방식보다 우선(중요도)

즉,

1. !important
2. 인라인 선언방식
3. ID 선택자
4. class 선택자
5. 전체 선택자
6. 상속 - 상속 받은 속성은 항상 우선하지 않음

## 단위

- % : 단위는 부모요소의 사이즈의 상대적으로 반응
- em : 단위는 font 크기에 영향을 받는다.
- rem : html에 지정된 font size만을 영향받음

## 박스 모델

- width : 요소의 가로 너비를 지정

* auto - 브라우저가 너비를 계산 (기본값)
* 단위 - px, em , cm 등 단위로 지정

- max-width : 요소의 최대 가로 너비를 지정

* 단위 px, em, % 등 기본값 none

- min-width : 요소의 최소 가로 너비

* 단위 px, em, % 등 기본값 0

- max-height : 요소의 최대 세로 너비를 지정

* 단위 px, em, % 등 기본값 none

- min-height : 요소의 최소 세로 너비

* 단위 px, em, % 등 기본값 0

## display

- 요소의 박스 타입(유형)을 설정
  블록 - div 등
  인라인 - span 등
  인라인블록 - input 등 기본적으로 수평으로 쌓이고 가로세로값을 가질수 있고 마진패딩 전부 사용가능

## overflow

- 요소의 크기 이상으로 내용(자식요소)이 넘쳤을 때, 내용의 보여짐을 제어

* visible : 넘친 부분을 자르지 않고 그대로 보여줌 (기본값)
* hidden : 넘친 부분을 잘라내고, 스크롤바를 이용하여 볼 수 있도록 함
* auto : 넘친 부분이 있는 경우만 잘라내고 스크롤 바를 이용하여 볼 수 있도록 함
* scroll : 넘친 컨텐츠는 잘리고, 스크롤 바가 생겨서 스크롤해서 볼 수 있습니다. 필요하던, 하지 않던간에 가로/세로 스크롤바가 모두 생깁니다.
