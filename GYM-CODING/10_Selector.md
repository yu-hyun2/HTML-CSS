# 기본 선택자

---

## ✔️ 전체 선택자 `* {}`

- 모두 선택
- 기본 스타일을 초기화 할 때 주로 사용

```css
/* *은 전체 선택을 의미 (전체 선택자) */
* {
  margin: 0;
  padding: 0;
}
```

<br>

## ✔️ 타입 선택자 `tagname {}`

- 특정 태그 이름을 가진 모든 요소 선택

```css
/* 태그명이 h1인 요소 모두 선택 (타입 선택자) */
h1 {
  color: blue;
}
h2 {
  color: green;
}
p {
  color: grey;
  font-weight: 400;
  text-align: center;
}
```

```html
<h1>애국가</h1>
```

![type selector](https://velog.velcdn.com/images/oigu529/post/96f22f06-9811-49cf-9ec9-f315ab2516dd/image.png)

이렇게 h1태그인 애국가 색만 변한 것을 확인

<br>

## ✔️ Class 선택자 `.classname {}`

- 중복으로 작성 가능
- class명을 갖는 모든 요소 선택

```css
/* class에 title을 갖는 모든 요소 선택(클래스 선택자) */
/* ex)) <h1 class="title"> */
.title {
  color: blue;
}
```

```css
/* Class 선택자 */
.red--text {
  color: red;
}
.blue--text {
  color: blue;
}
```

```html
<h1 class="title">애국가</h1>
<hr />
<h2>1</h2>
<p>
  <span class="red--text">동해</span> 물과
  <span class="red--text">백두산</span>이 마르고 닳도록<br />
  하느님이 보우하사 우리나라 만세<br />
  무궁화 삼천리 화려강산<br />
  대한 사람 <span class="red--text">대한</span>으로 길이 보전하세
</p>

<h2>2</h2>
<p>
  <span class="blue--text">남산</span> 위에 저
  <span class="blue--text">소나무</span> 철갑을 두른 듯<br />
  바람 서리 불변함은 우리 기상일세<br />
  무궁화 삼천리 화려강산<br />
  대한 사람 대한으로 길이 보전하세
</p>
```

![class selector](https://velog.velcdn.com/images/oigu529/post/01e70d65-0c62-420d-a7e2-94cf3b30bda8/image.png)

> `class`명에 지정한 색대로 변한 것을 확인

<br>

## ✔️ ID 선택자 `#idname {}`

- 고유한 하나의 태그에만 사용 ➡️ 웹 표준(오류는 안 남)

```css
/* ID 선택자 */
#title {
  font-size: 40px;
  color: darkslategray;
  background-color: yellow;
}
```

![id selector](https://velog.velcdn.com/images/oigu529/post/8fe87c50-8a34-4cf9-b07b-cf3ef686e279/image.png)

<br>

## ✔️ 그룹 선택자

- 여러 선택자 쉼표(,) 구분 나열로 한번에 정의 가능

```css
/* 그룹 선택자 */
h1,
h2 {
  text-align: center;
}
```

![attribute selector](https://velog.velcdn.com/images/oigu529/post/335d09ea-979c-4a3f-9671-1b358f059b2c/image.png)

> h1, h2 둘 다 center로 정렬됨을 확인

<br>

## ✔️ Attribute 선택자

- 속성이 존재하는 모든 요소 검색
- `=` 값이 일치
- `^=` 속성 값으로 시작하는 요소
- `$=` 속성 값으로 끝나는 요소
- `*=` 속성 값을 문자열이 포함하는 요소
- `~=` 속성 값을 단어로 포함하는 요소

```css
/* 속성이 존재하는 요소 
h2에 해당하는 요소 */
h2[class] {
  font-size: 30px;
}

/* 타겟이 있는 요소 */
a[target] {
  color: green;
}

/* 속성 값과 일치하는 요소 */
h2[class='naver-title'] {
  color: green;
}

/* 속성 값으로 시작하는 요소 */
h2[class^='google'] {
  color: blue;
}

/* 속성 값으로 끝나는 요소 */
a[href$='facebook.com'] {
  color: red;
}

/* 속성 값을 포함하는 요소 */
a[href*='www'] {
  text-decoration: none;
}

/* 속성 값이 단어로 포함된 요소 */
h2[class~='title'] {
  color: blue;
  font-weight: 300;
}
```

> ### `=`와 `*=`의 차이
>
> 포함하는 요소는 문자열에 해당 문자가 포함하는지
> 단어가 포함하는 건 단어의 존재여부 확인
>
> 그니까 문자열 안에 포함되기만 해도 되고 (`*=`)
> 공백으로 구분된 문자 즉, 단어가 있으면 (`~=`)인 것임
>
> ### `*="www"`
>
> 예를 들어 주소 `href="www.google.com"` 문자열에서 >`a[href*="www"]`라고 표기하면 검색이 가능하지만
> `a[href~="www"]`라고 표기하면 검색이 되지 않는다.
>
> ### `~="www"`
>
> `href="www google com"` 만약 이렇게 문자열이 구성되어 있다면  
> `a[href~="www"]`로 검색이 가능하다

![total attribute](https://velog.velcdn.com/images/oigu529/post/33b04c41-37c0-4479-81c4-c395a43c1862/image.png)

- `h2` 태그 중 `class`가 존재하면 폰트 사이즈 30
- `a` 태그 중 `target`이 존재하면 <span style="color: green;">green</span>
- `h2` 태그 중 `class`가 naver-title이면 <span style="color: green;">green</span>
- `h2` 태그 중 `class`가 google로 시작하면 <span style="color: blue;">blue</span>
- `a` 태그 중 `facebook.com`으로 끝나면 <span style="color: red;">red</span>
- `a` 태그 중 `www`를 포함하면 꾸미기 없음
- `h2` 태그 중 `title`이란 단어를 포함하면 <span style="color: blue;">blue</span>, 두께 300

<br>
<br>

# 결합자

---

## ✔️ 자손 결합자 ` `(공백)

- 하위 선택자 모두 선택

```css
/* 자손 결합자 */
section li {
  color: blue;
}
section span {
  color: red;
}
```

<br>

## ✔️ 자식 결합자 `>`

- 하위 선택자만 선택

```css
/* 잘못된 자식 결합자 */
section > li {
  color: yellow;
}
```

```css
/* 옳은 자식 결합자 */
ul > li {
  color: yellow;
}
```

> `section > li`으로 하면 적용이 안 됨 ➡️ 자손 결합자로 바로 하위가 아니라서 자식 결합자로 사용하고 싶으면 `ul > li` 또는 `section > ul > li`로 해야 적용됨
>
> 할머니 - 엄마 - 나
> 할머니가 나를 낳으신 게 아니라 엄마가 나를 낳으셨잖음

<br>

## ✔️ 일반 형제 결합자 `~`

- 첫 번째 요소를 같은 부모(상위)로 가지는 두 번째 요소들 선택

```css
/* <p>태그의 뒤에(아래) 나오는 모든 <span>요소 */
p ~ span {
  color: red;
}
```

## ✔️ 인접 형제 결합자 `+`

- 형제 중 첫째

```css
/* <h2>태그 바로 뒤에 위치하는 <p>요소 */
h2 + p {
  color: blue;
}
```

- 이렇게 응용 가능

```css
.first + li {
  color: green;
}
```

```html
<!-- first 바로 밑의 two가 green 색으로 바뀜 -->
<li class="first">one</li>
<li>two</li>
<li>three</li>
```
