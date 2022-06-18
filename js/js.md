# Javascript

- 문법
  - javascript 언어 문법
  - 문법의 내용
    - 데이터/변수/연산자
    - 명령문
    - 함수
    - 배열/객체/Class
    - 추가 문법

- 활용
  - HTML/CSS/Js 종합 활용
  - HTML DOM
  - Open API - 객체

## JS basic

- version
  - ES5
  - ES6

- 작성방식
  - External : js 파일 생성
  - internal
    - HTML 파일에 js 코드를 작성
    - js 코드 블럭을 따로 구분해서 작성
  - Inline 
    - HTML tag에 js 코드를 작성

- 작성위치
  - js 실행되는 시점에 HTML이 로딩되어 있어야함 
  - js 실행되는 방식 : 최초 한번만 실행됨

## JS 문법

### 데이터/변수/연산자

- 데이터
  - 숫자
  - 문자
```
숫자 : 0, 1, 2, 3, 4, 5 ...
문자 : 가, 나, 다 ... , a, b, c ...
```

- 데이터 타입(종류)
  - 숫자 : 정수, 실수 ...
  - 문자
    - 코드상에서 문자는 따옴표로 묶임
    - 낱개 글자, 묶음 글자 ...
```
1 + 1 = 2

'a' + 1 = 'a1'

'1' + 1 = 11
```

** 자바스크립트는 데이터 타입을 엄격하게 구분하지 않음 

- 변수(variable)
  - 데이터를 저장하는 공간
  - 변수는 선언/정의를 한 이후에 사용
  - 변수 선언 예약어
    - var(ES5) : 타입 구분 안함, 데이터 변경 자유로움
    - let(ES6) : 타입 구분 안함, 데이터 변경 자유로움
    - const(ES6) : 타입 구분 안함, 데이터 변경 불가능

```
JAVA
정수 변수 선언 : int number1;
실수 변수 선언 : float number2;
문자 변수 선언 : char text;

ES
정수 변수 선언 : var number1; | let number1;  | const number1;
실수 변수 선언 : var number2; | let number2;  | const number2;
문자 변수 선언 : var text;    | let text;     | const text;
```

- 연산자

- 산술연산자
  - +, *, -, /
  - % : 나머지연산

- 할당(대입)연산자
  - = : 값을 변수에 저장
```
const PI = 3.141592;
```

- 산술+대입연산(재귀)
```
let a = 10;

a = a+5
a += 5
```
** 산술+대입 연산이 반복 실행되면 일정 값을 지속적으로 연산

- 카운터
```
a += 1 => a++

a -= 1 => a--
```

- 비교연산


### 명령문

### 함수

### 배열/객채/Class

## JS 활용