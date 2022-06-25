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
(3) | 자손 요소 | 형제 요소   
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

### Media

#### image(이미지)

#### video(영상)

## HTML Structure

### Semantic

### Layout

# CSS
