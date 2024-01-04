> ### 개발자도구(F12)에서 폰트 설정

- Elements -> html 선택 -> style -> element.style{} 안에 font-family 입력하면 폰트 목록이 나옴
  > ![개발자도구font](https://velog.velcdn.com/images/oigu529/post/7f0cf7cc-346a-4aa1-a93a-d25edac06991/image.png)

<br>

## CSS에서 폰트설정

```html
<style>
  /* html {
    font-family: serif, monospace;
  } */
  .title {
    font-size: 25px;
  }
  .content {
    font-size: 15px;
  }
  /* 기울임 */
  .font-iltalic {
    font-style: italic;
  }
  /* 굵게 */
  .font-weight-bold {
    font-weight: bold;
  }
  /* 굵기 조정 */
  .font-weight-300 {
    font-weight: 300;
  }
  /* 소문자를 작은 대문자로 바꿈 */
  .font-variant {
    font-variant: small-caps;
  }
</style>
```

<br>

## html에서 적용

- 폰트 사이즈와 이탤릭체를 같이 적용하고 싶을 때 밑의 코드처럼 작성하면 됨!

```html
<body>
  <h2 class="title">나만 없어 고양이</h2>
  <p class="content">
    1. 갖고 싶다 고양이 나만 없어 고양이 다 있는데 고양이 고양이 야옹
  </p>
  <p class="content font-iltalic">
    2. 갖고 싶다 고양이 나만 없어 고양이 다 있는데 고양이 고양이 야옹
  </p>
  <p class="content font-weight-bold">
    3. 갖고 싶다 고양이 나만 없어 고양이 다 있는데 고양이 고양이 야옹
  </p>
  <p class="content font-weight-300">
    4. 갖고 싶다 고양이 나만 없어 고양이 다 있는데 고양이 고양이 야옹
  </p>
  <p cl
```

![font style](https://velog.velcdn.com/images/oigu529/post/eaf3a449-22a1-45c7-b6bc-0d70922b989f/image.png)

.. 반복적으로 써 놓으니 약간의 광기가 보이지만... 순서대로 출력한 결과이다..

1. 폰트 사이즈 15
2. 폰트 사이즈 15 + 이탤릭체
3. 폰트 사이즈 15 + 굵게
4. 폰트 사이즈 15 + 굵기 가중치 300

특히 마지막 줄`HEELO, MY SWEETHEART`은
`대문자, 소문자` 였으나 `대문자, 작은 대문자`로 바뀜
➡️ 오.. 생소한 스타일

<br>
<br>

# 웹 폰트

---

## [Google Fonts](https://fonts.google.com/)

폰트를 골라 굵기 선택을 하면 오른쪽에 어떻게 사용할 건지 체크(`link` or `import`)
![google](https://velog.velcdn.com/images/oigu529/post/29d26117-228d-49b9-928e-154254330c9b/image.png)

html의 style 최상위에 얹어두고

```html
<style>
  @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+KR:wght@100;200;300;400;500;600;700&display=swap');
</style>
```

html에 이 링크 적용

```css
font-family: 'IBM Plex Sans KR', sans-serif;
```

![font ibm](https://velog.velcdn.com/images/oigu529/post/a0d02ac9-559d-4b62-a0b7-5939833f07c7/image.png)

폰트 바뀐 거 확인

<br>
<br>

# 단위

---

## ✔️ rem

- 최상위 요소 폰트 사이즈의 배수

```css
.subtitle {
  font-size: 20px;
}
.subtitle-rem {
  font-size: 2rem;
}
```

`2rem`이라는 건 루트 글꼴 크기의 2배라는 의미
루트 요소는 `html`이니까 html css의 `font-size`보다 두 배 값이라는 거

```css
html {
  /* font-family: serif, monospace; */
  font-family: 'IBM Plex Sans KR', sans-serif;
  font-size: 16px;
}
```

즉, 이 코드에서 `2rem`은 `16 * 2 = 32px`이 됨

![요소검사](https://velog.velcdn.com/images/oigu529/post/cb5e6cb0-a539-4ff7-8792-1907c8534fc2/image.png)

요소 검사를 누르고 확인할 요소를 마우스 오버하면 폰트 사이즈 확인 가능
![rem](https://velog.velcdn.com/images/oigu529/post/bd377172-adab-452d-a28e-5ea2c0662863/image.png)

짠 진짜 32px임을 확인 가능

<br>

## ✔️ em

- 자기 자신 폰트 사이즈 기준으로 배수
- 2em은 자기 자신의 폰트 사이즈의 두 배 값을 가짐

> ⭐ 주의할 점
> p 태그는 부모 태그의 font-size를 상속받아서 rem과 엄연히 다름
> 최상위 폰트 사이즈가 16이어도 em의 부모 태그의 폰트 사이즈가 10이라면 2em은 20이 되는 것임

예를 들어

```css
html {
  /* font-family: serif, monospace; */
  font-family: 'IBM Plex Sans KR', sans-serif;
  font-size: 16px;
}

.subtitle-em {
  font-size: 2em;
}
```

이렇게 html의 font-size를 상속받는 2em은 16 \* 2 = 32px가 되고

```html
<h2>em</h2>
<p class="subtitle-em">
  3. 갖고 싶다 고양이 나만 없어 고양이 다 있는데 고양이 고양이 야옹
</p>
```

<br>

만약에

```css
.article {
  font-size: 10px;
}
```

를 css에 추가해서

```html
<h2>em</h2>
<div class="article">
  <p class="subtitle-em">
    3. 갖고 싶다 고양이 나만 없어 고양이 다 있는데 고양이 고양이 야옹
  </p>
</div>
```

이렇게 `article`이라는 부모 요소가 생기면
`article`의 font size인 10px가 기준이 되고 `subtitle-em`은 20px 값을 가진다.

![em](https://velog.velcdn.com/images/oigu529/post/bd3ab2c4-3d26-4b69-a99f-4faa75cbd8ab/image.png)

> 최상위 요소 `html`을 부모로 갖는 `rem`은 32px, 부모 요소가 `article`인 `em`은 20px임을 확인

<br>

## ✔️ Viewport

viewport: 화면 사이즈

- Viewport Width
- Viewport Height

예를 들어 가로 1200px, 세로 1600px이면,

- 100vw = 1200px
- 50vw = 600px
- 100vh = 1600px
- 50vh = 800px

<br>
<br>

# 글자 색상

---

![click](https://velog.velcdn.com/images/oigu529/post/fa55fddc-c048-4f25-b8b6-ed27afb17e26/image.gif)

색상에 마우스 오버하면 색을 선택할 수 있는데, 특히 표시 형식을 다양한 방식으로 표현할 수 있다.

![title color](https://velog.velcdn.com/images/oigu529/post/3140374b-323e-40f2-a9c6-6a11730b17b4/image.png)

<br>
<br>

# 글자 속성

---

### 정렬

```css
/* 가운데 정렬 */
.text-center {
  text-align: center;
}
/* 오른쪽 정렬 */
.text-right {
  text-align: right;
}
/* 왼쪽 정렬 */
.text-left {
  text-align: left;
}
```

![align](https://velog.velcdn.com/images/oigu529/post/35539c35-1114-4382-91d1-9b9a96d7ffca/image.png)

<br>

### 줄간격

```css
html {
  font-size: 16px;
}
.article {
  line-height: 2.2rem;
}
```

<br>

### 글자 간격

```css
letter-spacing: 1px;
```

<br>

### 단어 간격

```css
word-spacing: 8px;
```

<br>

### 들여쓰기

```css
text-indent: 8px;
```

<br>

### 소문자 변환

```css
.transform-case {
  text-transform: lowercase;
}
```

<br>

### 하이퍼링크처럼 파랭이밑줄

```html
<a href="#">자주개자리</a>
```

<br>

### list 스타일 변경

```css
ul {
  list-style: circle;
}
```

<br>

![토끼풀](https://velog.velcdn.com/images/oigu529/post/d595ab7d-60b1-4e2a-9609-68cbe4e0795d/image.png)

참고...
