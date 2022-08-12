# HTML Coding Style Guide

## Use Lower Case Element Names.

- Mixing uppercase and lowercase names is bad.
  대문자와 소문자를 혼용하면 좋지 않습니다.
- Developers normally use lowercase names.
  개발자는 일반적으로 소문자 이름을 사용합니다.

## Close All HTML Elements

- Recommend closing all HTML elements.

#### Bad

```
<SECTION CLASS="test">
  <P>test</P>
</SECTION>
```

#### Good

```
<section class="test>
  <p>test</p>
</section>
```

## Close Empty HTML Elements

- In HTML5, it is optional to close empty elements.
  html5에서는 빈 요소를 닫는 것이 선택사항입니다.
- However, the closing slash (/) is REQUIRED in XHTML and XML.
  그러나 XHTML 및 XML에서는 닫는 슬래시(/)가 필요합니다.
- We don't use XHTML and XML. So, don't close empty element.
  우리는 XHTML, XML을 사용하지 않으므로 빈 요소를 닫지 않습니다.

#### Example

```
<meta charset="utf-8">
<br>
<hr>
<input type="text">
```

## Quote Attribute Values

- Quoted values are easier to read. we must use quotes if the value contains spaces.
  따옴표로 묶인 값은 읽기 쉽습니다. 값에 공백이 있으면 따옴표를 사용해야 합니다.

#### Bad

```
<table class=test>
<table class=table test>
```

#### Good

```
<table class="test">
```

## 이미지 속성

- 항상 이미지에 `alt` 속성을 추가해야 합니다.
- `웹 접근성(장애인 배려)`과 `어떤 이유로 이미지가 표시되지 않았을 경우`에 매우 중요합니다.
- 로드하기 전에 브라우저가 이미지 공간을 예약할 수 있게 이미지 너비와 높이를 정의합니다.
- 단순한 장식 이미지에는 `alt` 속성을 사용하지 않습니다.

#### Bad

```
<img src="test.jpg">
```

#### Good

```
<img src="test.jpg" alt="HTML5" style="width:128px;height:128px">
```

## 공백과 등호

- 등호 주위에 공백을 사용하지 않습니다.

#### Bad

```
<link rel = "stylesheet" href = "style.css">
```

#### Good

```
<link rel="stylesheet" href="style.css">
```

## 긴 코드 라인 피하기

- HTML 편집기를 사용할 때, 좌우로 스크롤하면서 코드를 읽는 게 불편하므로, 긴 코드 행을 피합니다.

## 메타태그를 제대로 넣기

## 주석 입력

- 콘텐츠 시작과 끝을 한 줄로 작성해줍니다.

```
<!--comment start-->
<section id="comment">
  <p>test</p>
</section>
<!--./comment end-->
```

- 두 줄 이상 걸쳐있는 주석은 다음과 같이 작성해줍니다.

```
<!--
  <section id="comment">
    <p>test</p>
  </section>
-->
```

## style sheets

- 유지보수를 위해 스타일 시트는 무조건 외부로 연결합니다.
- 절대 인라인으로 스타일을 주지 않습니다.
- `css/style.css(style.scss)`를 메인으로 사용합니다.

#### bad

```
<style>
#comment {color:blue}
</style>

<section id="comment">
  <p style="background:skyblue">test</p>
</section>
```

#### good

```
<link rel="stylesheet" href="style.css">
```

## javascript

- 유지보수를 위해 자바스크립트 또한 무조건 외부로 연결해줍니다.
- `js/main.js`를 메인으로 사용합니다.
- 상단이 아닌 `body` 안에 넣습니다.

## 파일 이름

- `소문자`로 `공백 없이` 사용합니다.
- 일부 웹 서버에서는 파일 이름의 대소문자를 명확하게 구분하기 때문입니다.
- 공백이 있을 경우 `아래`처럼 작명합니다.

#### Example

`korea-good.jpg(Good)`

`Korea good.jpg(Bad)`

## HTML 유효성(웹 표준)

- <a href="https://validator.w3.org/nu/">W3C HTML Validator</a>같은 툴을 활용하여 유효성을 검증합니다.

## 엔티티(Entity) 참조

- 엔티티 참조를 사용하지 않는다.
-
