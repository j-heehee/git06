# HMTL

- Contents

  - Text
  - Media
    - Image, Video, Audio

- Structure
  - Semantic : 의미있는 구조
  - Layout

## HTML basic

- HTML : Hyper Text Markup Language

  - Hyper Text : 하이퍼링크로 연결된 문서 → 웹페이지(컨텐츠, 구조)
  - Markup : 표시
  - Language : 언어

- HTML 문법
  - 명칭 : Tag / Element
  - 구성 : 시작태그 ~ 종료태그
  - 종료태그가 없는 태그 : 빈태그(Empty Element)

```
<tag> content </tag> : Element

<tag ...> : Empty Element
```

- HTML 속성(attribute)
- HTML Element를 표시할때 필요한 추가정보 입력
- name="value"

```
<a href="https://www.naver.com">네이버</a>

<img src="photo.jpg">
```

## HTML Basic Structure

```
<!DOCTYPE html>
<html>
  <head>
    <title></title>
  </head>
  <body></body>
</html>
```

### DOCTYPE

- HTML 문서 타입
  - HTML 버전
  - HTML5 표준

### Head - 웹사이트 기본 정보

- meta : 웹사이트 관련 정보(검색엔진)
- title : 웹사이트 제목

### Body - 웹사이트 컨텐츠

- 웹사이트에 contents, structure... 표시하는 모든 태그

## HTML Contents

### Text

#### heading(제목)

- h(heading) : 제목태그
- 1 ~ 6 단계로 표시됨

#### paragraph(단락)

- p(paragraph) : 단락태그
- 강제줄바꿈, 강제 공백은 이식되지 않고 공백 한 칸으로만 인식
  - line break : br(강제줄바꿈 태그)
  - space : &nbsp;(강제 공백 엔터티(Entity))
- hr(horizontal rule) : 수평선 긋기
  - 단락을 선의 형태로 구분

#### list(목록)

- ul(Unordered List) : 순서없는 몰록
- ol(Ordered List) : 순서있는 목록
- li(List Item) : 목록 항목

\*\* 포함관계(Nested Sructure)

- 태그안에 다른 태그들이 포함되는 것
- 포함하는 요소
  - 조상요소(Ancestor)
  - 부모요소(Parent)
- 포함되는 요소
  - 자식요소(child)
  - 자손요소(Descendant)
- 옆에 나란히 있는 요소
  - 형제요소(sibling)

```
(1) <html>
(2)   <body>
(3)     <h1>내용 제목</h1>
(4)     <p>
(5)       단락내용<br>
        </p>
      </body>
    <html>
```

(1) 조상 요소 | 기준 요소 | 조상 요소  
(2) 조상 요소 | 자식 요소 | 부모 요소  
(3) 　　　　　| 자손 요소 | 형제 요소  
(4) 부모 요소 | 자손 요소 | 기준 요소  
(5) 기준 요소 | 자손 요소 | 자식 요소

- Description List(설명 목록)
  - dl(desciption list)
  - dt(desciption title) : 항목
  - dd(desciption data) : 항목에 대한 설명

#### table(표)

- table
- thead(table head) : 표 상단 - 제목
- tbody(table body) : 컨텐츠, 데이터
- tr(table row) : 행(줄)
- th(table header) : 제목
- td(table data) : 열(칸)
- html tables generator를 이용하면 효율적임

#### hyper link(하이퍼링크)

- a(anchor)
- 기본 속성 : href(hypertext reference) : 연결할 위치(웹페이지)

- 링크 이동 위치
  - 외부링크
  - 내부링크 : Bookmark

### Media

#### image(이미지)

- img(image)
  - 빈 요소
- 기본 속성
  - src(source) : 이미지 파일 이름, 위치
  - alt(alternative text) : 대체 텍스트 - 이미지가 화면에 표시되지 않을 때, screen reader

```
<img src="photo.jpg" alt="제주도 서귀포 바닷가 배경 사진">
```

#### video(영상)

- video, source
- 속성

  - video 태그 : on/off 형태 attribute

    - controls : 동영상 제어 버튼
    - autoplay : 자동 재생
    - muted : 음소거
    - loop : 반복 재생

  - source 태그
    - src : 파일 이름, 경로
    - type : 미디어 형식

- Youtube 영상

## HTML Structure

### Semantic

- header
  - logo, login ...
- nav(igation)
  - menu
- section
  - 본문 영역
- article
  - 본문 영역
- aside
  - 본문 영역, 부수적인 컨텐츠
- footer
  - 연락처, 주소, 회사 이름 ...

### Layout

- Block & Inline
  - Block 요소
    - 태그가 브라우저에 표시될때 각 태그 영역이 새 줄에서 표시
    - 태그 영역이 부모요소에 전체 채워짐
  - Inline 요소
    - 태그가 브라우저에 표시될때 각 태그 영역이 같은 줄에서 표시
    - 태그 영역이 콘텐트에 맞춰짐

### container element

- div(sion)
- block
- span
- inline

## 경로 지정 방식

- 파일 위치, 인터넷 주소(URL)
- 상대 경로
  - 리소스 파일을 사용하는 HTML 파일 기준
  - html 파일 위치에 따라 주소(URL) 변경
  - root(/) 폴더를 기준으로 주소 적용 => root 상대 경로

```
[root(/)] - [html1] - home.html
          - [html2] - [about] - about.html
          - [images] - photo.jpg

1) home.html -> photo.jpg
- ../images/photo.jpg
- /images/photo.jpg

2) about.html -> photo.jpg
- ../../images/photo.jpg
- /images/photo.jpg
```

- 절대 경로
  - 이미지를 표시하는 HTML 페이지가 기준이 아니고, 해당 서버가 기준
  - 서버부터 주소(URL)를 사용하기 때문에 변동이 없음.

```
image.com

[root(/)] - [html1] - home.html
          - [html2] - [about] - about.html
          - [images] - photo.jpg

1) home.html
- www.image.com/images/photo.jpg

2) about.html
- www.image.com/images/photo.jpg
```

## 강조 태그, 기타 태그

- 텍스트 특정 부분 강조
  - strong : 강한 강조
  - em(phasize) : 일반 강조
  - mark : html5 버전, block 강조
- 텍스트를 표현할 때 부족한 태그를 보완하는 태그
  - i(talic)
  - b(old)

# CSS

- content styling

  - text styling
  - media styling

- layout(structure styling)
  - 가로배치(flexbox)

## CSS Basic

- CSS : Cascading Style Sheet

```
h1 {color:blue;font-size:20px;}

h1 {
  color:blue;
  font-size:20px;
}
```

## Selector(선택자)

- 선택자로 HTML 요소를 선택
- HTML 요소 선택 방법
  - Simple Selector(단순 선택자)
    - Tag/Element 이름 사용
    - class 이름 사용
    - id 이름 사용

```
<a href="https://www.naver.com" class="naver">네이버</a>
<a href="https://www.daum.net" id="daum">다음</a>

/* a 태그 2개 모두 red 적용 */
a {
  color:red;
}

/* a 태그 각각 다른 color 적용 */
.naver {
  color:green;
}
#daum{
  color:blue;
}
```

### id, class 이름의 특징

- id

  - 같은 HTML 페이지에서 고유(유일)해야 함
    - 프로그래밍 언어의 변수와 연결 가능성이 있음
  - HTML 요소에 여러개의 id 이름 사용 불가능

- class
  - 같은 HTML 페이지에서 여러번 사용 가능함
  - HTML 요소에 여러개의 class 이름 사용 가능

```
<p class="paragraph">단락1</p>
<p class="paragraph">단락2</p>  (O)
<p id="content">단락3</p>
<p id="content">단락4</p>       (X)
```

### CSS 선택자 우선순위

- cascading 규칙
  - 동일한 대상에 여러 스타일이 적용될 때 제일 마지막에 적용된 스타일이 반영
- 선택자 우선순위
  - 선택자 종류에 따라 css 적용 우선순위가 다르게 정의
  - cascading 규칙에 따르지 않고 css를 적용할 때 사용
- 우선순위 점수
  - inline : 1000
  - id : 100
  - class : 10
  - tag : 1

### Test Styling

#### Color

```
h1{
  color:blue;
}
```

#### Text alignment

```
p{
  text-align:center;
}
```

- 정렬 값 : left, center, right, justify(양쪽맞춤)

- word-break : 단어 중간에 줄바꿈 property

```
p{
  word-break:break-all;
}
```

#### Text Decoration

```
h1{
  text-decoration:underline;
}


h1{
  text-decoration:line-through;
}


h1{
  text-decoration:overline;
}

a{
  text-decoration:none;
}
```

#### Text Spacing

```
p{
  text-indent:16px;
}

h2{
  letter-spacing:5px;
}

p{
  word-spacing:3px;
}

p{
  white-space:nowrap;
}
```

- line-height
  - 텍스트 줄을 포함한 줄 높이
  - 값 : px, 배수(소수점을 포함한 값)

\*\* 조상요소나 부모요소에 CSS 속성을 적용했을 때, 자식요소에도 적용되는 것을 상속

- HTML Element 중에 상속되지 않는 태그가 있음
- CSS 속성중에 상속되지 않는 속성이 있음

#### Font Family

- css 파일이 브라우저에서 랜더링되기 때문에 폰트 파일을 클라이언트 PC에서 찾음
  - 다수의 클라이언트 PC에 설치될 만한 폰트를 선택(Web safe)
- font-family 속성에 값으로 정해진 폰트 종류를 차례대로 찾음(Fallback)

- 서버에서 폰트를 사용할 수 있게 하는 기능
  - Web Font

- 구글 폰트

- 폰트 종류(저작권)
  - 폰트 파일 포함 여부

#### Font size

- font-size
- 폰트 크기
- px

#### Font Style

- font-style
- 기울임꼴 설정
- italic 값

#### Font weight

- font-weight
- 굵기
- normal/bold
- 단위없는 100단위 숫자 값 사용

#### Link Style
- a 태그가 4가지 상태를 구분함
- Link, visited, hover, active
```
<a href="#" class=link>naver</a>

a:link{}
.link:visited{}
a:hover:{}
a:active{}
```

### Media Contents styling
- Image, Video
  - Box Model 적용
  - 위치 지정

### Layout styling
- Element 영역
  - Block, Inline Element
- Element 영역 Styling
  - Box Model
- Element 배치
  - 배치 지정
    - 인접해있는 박스들의 관계
    - 인접해있는 박스들 사이에 영향 
  - 위치 지정 
    - 박스의 위치를 단독으로 지정

#### Box Model
- Box Model 구성요소
  - content(width/height), padding, border, margin

- inline 요소에 box model 적용
  - width/height : 적용 안됨
  - margin : 위아래 적용 안됨, 좌우 적용됨

- 박스 크기 계산
  - 박스 모델 구성요소(width/height + padding + border)의 크기 합 => 박스의 전체 크기
Ex) width:300px, padding 4방향 모두 20px, border 4방향 1px, margin 4방향 10px => 박스의 실제 크기 : 300 + 40 + 2 = 342px

- box-sizing 속성
width의 기준을 content 또는 전체크기 중에 선택

```
div{
  width:300px;
  padding:20px;
  border:1px solid black;
  box-sizing:content-box; /* default */
}

300 + 40 + 2 = 342px /* width:300px => content 영역의 크기 */

div{
  width:300px;
  padding:20px;
  border:1px solid black;
  box-sizing:border-box;
}

x + 40 + 2 = 300px /* width:300px => box 전체 크기 */ 
                   /* content 영역의 크기 : x = 300 - 40 - 2 */
```

##### width/height
- block 요소
  - width는 부모요소에 채워짐
  - height는 contents 또는 자식요소에 맞춰짐
- px
  - 수치 값으로 크기 고정
- %
  - 부모 요소를 기준으로 일정 비율 크기만큼 지정
  - height는 적용이 되지 않음
- auto
  - width/height 자동으로 크기 지정
  - width/height의 원래 특성으로 적용(default)

##### padding
- 안쪽 여백
```
padding-top
padding-right
padding-bottom
padding-left
(** 방향 순서 : top을 기준으로 시계방향순)

padding:10px 20px 30px 40px; → 4방향 각각 적용

padding:10x 20px 30px; → 2번째값 좌우 공통 적용

padding:10px 20px; → 1:위아래 공통/2:좌우 공통

padding:10px; → 4방향 공통 적용
```

##### margin
- margin 사용 방법은 padding과 동일
- margin collapse(겹침/상쇄)
  - 위아래에 인접한 박스의 margin이 상쇄되는 현상
  - 두 여백중 큰 쪽 여백만 적용
  - 좌우로 인접한 박스는 양쪽의 margin이 모두 적용되어 합쳐짐

##### border
- 굵기, 모양, 색
```
border:1px solid red;

border-top:1px solid red;
boder-right
border-bottom
boder-left
```
##### background
- 배경색, 배경 이미지 표시
- 배경은 box model 요소중 content, padding 영역까지 적용
```
background-color:red;

background-image:url(이미지주소);
background-repeat:no-repeat;
background-position:10px 20px;
background-attachment:fixed;
```
- background-repeat
  - repeat(default), repeat-x, repeat-y, no-repeat

- background-position
  - px
  - left, center, right
  - top, center, bottom
  - 배경이미지의 위치 지정은 이미지 반복이 안될 때 적용

- background-attachment
  - 배경 이미지 고정
  - fixed

#### display
- 박스의 표시 속성을 변경해서 표시
```
display:inline; /* block 요소가 inline요소의 특성으로 화면에 표시 */
display:block; /* inline 요소가 block요소의 특성으로 화면에 표시 */
display:inline-block; /* inline과 block의 특성을 모두 표시 : 나란히 표시, 박스모델 */
```

### layout 배치
- float
- flex
- grid

#### flexbox
- HTML Element가 포함 관계로 구성
- 부모요소에 flex 설정, 배치관련 속성들을 적용
```
<div class="flex-container">
<div>div1</div>
<div>div2</div>
<div>div3</div>

.flex-container{
  display:flex;
  flex-direction:column; /*박스 배치 방향*/
  flex-wrap:wrap; /*박스 배치 줄바꿈*/
  justify-content:center; /*박스 배치 가로 정렬, 간격*/
  align-items:center; /*박스 배치 세로 정렬*/
}
```

#### position
- 박스 위치 단독 지정
- top, right, bottom, left 위치 지정 속성과 같이 사용

- relative
  -  박스 원래 위치에서 좌표 크기만큼 이동
  - 요소의 일반 흐름에서 제외되지 않음

- absolute
  - position 속성이 적용된 가장 가까운 조상요소를 기준으로 위치 지정
  - 요소의 일반 흐름에서 제외됨
  - 문서에서 제외되지 않음

- fixed
  - browser를 기준으로 위치 지정
  - 요소의 일반 흐름에서 제외됨
  - 문서에서 제외됨

#### z-index
- 박스가 겹칠 때 앞뒤 순서 지정
- 값은 단위 없는 정수(양수, 음수)를 사용
- z-index를 사용할 때는 position 속성이 적용되어 있어야 함
- 숫자가 크면 앞으로 나옴

## 반응형 웹
- 다양한 디바이스의 화면에 컨텐츠, 레이아웃이 잘 보이도록 스타일 구현
- OSMU(One Source Multi Use)
  - 하나의 HTML source, 여러개의 CSS source

### 뷰포트
- 모바일 디바이스 화면에 웹 페이지 컨텐츠나 레이아웃이 잘 보일 수 있도록 하는 기능
- 뷰포트가 없을 때는 PC에 최적화된 레이아웃이 모바일 디바이스 화면에 보이게 됨

### 미디어쿼리
- 특정 조건(상황)에 맞는지 비교
- 특정 조건에 맞으면 포함되어 있는 CSS 코드 블럭을 실행
```
@media screen and (max-width:600px){}
@media screen and (min-width:600px){}

max-width:600px → 600px보다 작은 범위
min-width:600px → 600px보다 큰 범위
```
디바이스 스크린의 해상도는 가로 해상도를 기준
- PC Monitor
  - 1920 * 1080px : Full HD(1K)
  - 3840 * 2160px : 4K
  - 1280 * 720(1024)
  - 1024 * 768

- Tablet
  - 1920 * 1080
  - 1280 * 720
  - 1024 * 768

- Mobile
  - 400 * 800
  - 320 * 640

- Breackpoint
  - 화면 크기에 따라 CSS가 다르게 적용되는 해상도 지점
  - 위 해상도 사례에서 1024, 720, 320 해상도가 breakpoint로 선택될 수 있음

## color 값
CSS에서 사용할 수 있는 color 값
- red, blue, black
- #a1eb35 : 16진수 값
- rgb(0255, 0255, 0~255) : 10진수 값
```
컴퓨터에서 사용하는 진수:2진수
2진수 데이터 : 01101110

bit : 2진수 1자리 저장(표현)공간 / 컴퓨터 데이터의 최소 단위
8bit = 1byte : 정보 표현의 최소단위 / 표현가능 개수 : 2^8 = 256

RGB : Red, Green, Blue - 화면(screen) / 가산 혼합
CMYK : Cyan, Magenta, Yellow, Black - 인쇄 / 감산 혼합

Red(1byte), Green(1byte), Blue(1byte) => 24bit 트루컬러(2^24)

16진수(0~9, a,b,c,d,e,f)
2진수 4bit => 16진수 1bit
24자리 2진수 => 6자리 16진수
Ex) #1a3cff, #555555 => #555, #55ffdd => #5fd

cf) #ffffff : white / #000000 : black / #555555, #f9f9f9 : grey

10진수
함수 사용 : rgb(red, green, blue)
10진수 범위 : 0~255

Ex) rgb(100, 230, 58)
```

## image format
비트맵
- 확대하면 깨짐
- jpg(색표현), gif(투명배경, 애니메이션), png(투명배경)

벡터
- 확대해도 안깨짐
- svg