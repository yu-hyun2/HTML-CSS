# position 속성

HTML 요소 배치하는 방법 지정

---

실습을 해 봅시다
Block 요소들로 html 구조를 작성하고 css 설정으로 박스 색상 설정

```css
main,
section,
article,
div {
  border: 1px solid black;
  padding: 20px;
}
main {
  background-color: #4d5159;
}
section {
  background-color: #7b838c;
}
article {
  background-color: #c7cfd9;
}
div {
  background-color: #a4b3bf;
}
```

<br>

## ✔️ static(기본값)

- 일반적인 흐름을 따라 배치
- 위치 속성 적용 불가

> 위치 속성을 적용하고 싶으면 **`position: relative;`**를 사용

```css
.static {
  position: static;
}
```

![static](https://velog.velcdn.com/images/oigu529/post/cc0cbfa2-1f00-4426-bd66-5f1abad0a6a5/image.png)

> #### static은 기본값이라 변하는 게 없음

<br>

## ✔️ relative

- 일반적인 흐름을 따라 배치
- 위치 속성으로 자신의 static 위치에서 상대적인 위치에 배치 가능

```css
.static {
  position: static;
  top: 0px;
  left: 20px;
}
.relative {
  position: relative;
  top: 0px;
  left: 20px;
}
```

![relative](https://velog.velcdn.com/images/oigu529/post/bbb6f048-2ad8-4aac-9355-bf6829f245bc/image.png)

> #### 같은 위치 속성을 부여했지만, relative만 기존 자신의 위치에서 left에 20px만큼 공간이 생김

<br>

## ✔️ absolute

- position 속성을 가지고 있지 않은 부모 기준으로 배치
- 부모 중 `relative`, `absolute`, `fixed`인 태그가 없으면 가장 위 태그 `<body>`가 기준이 됨

### 1. position만 적용했을 때

```css
.absolute {
  position: absolute;
}
```

![absolute](https://velog.velcdn.com/images/oigu529/post/b03cb54c-26f2-44d8-89aa-bdbf67d29c1e/image.png)

### 2. position + 위치

```css
.absolute {
  position: absolute;
  right: 20px;
}
```

![absolute2](https://velog.velcdn.com/images/oigu529/post/95bdec02-0aa8-4b85-9c3a-599ab404dd43/image.png)

<br>

## ✔️ fixed

- 스크린의 뷰포트를 기준으로 한 위치에 배치
- 스크롤해도 고정된 자리에 위치
- 사이트에서 챗봇 상담 떠있는 느낌임

> **뷰포트(viewport)**: 웹 페이지가 브라우저 화면상에서 실제로 표시되는 영역

![fixed](https://velog.velcdn.com/images/oigu529/post/71a82178-5806-48f6-84d1-1dc41ef9df56/image.gif)

<br>

## ✔️ sticky

- 일반적인 흐름에 따라가다가 임계점에 이르면 박스를 화면에 고정
- 엑셀의 행고정마냥 스크롤되어도 움직이지 않는 고정된 자리를 가짐
- **위치 속성 top을 적용해야 고정이 되고** top외에 다른 속성 사용 불가

### 1. top 0px

```css
.sticky {
  position: sticky;
  top: 0px;
}
```

![0px](https://velog.velcdn.com/images/oigu529/post/89836431-0d11-4416-b207-3aa72e777bf6/image.gif)

### 2. top 50px

```css
.sticky {
  position: sticky;
  top: 50px;
}
```

![50px](https://velog.velcdn.com/images/oigu529/post/0df22c35-7fa5-4d3b-9364-d3eecb14e0dc/image.gif)

> top만 적용이 가능하고 적용한 px만큼 간격이 생기는 것을 볼 수 있다.

<br>
<br>

# 기타 속성

---

## ✔️ 위치

- top
- bottom
- left
- right

<br>

## ✔️ z-index

- 어느 HTML 요소가 앞, 뒤에 나올지 배치 순서 결정
- 앞으로 보내기 뒤로 보내기 같은 기능
- position 속성이 적용된 요소에서만 작동
  - `relative`, `absolute`, `fixed`

<br>

### z-index 적용 전(기본값 0)

```css
.absolute {
  position: absolute;
  right: 20px;
  background-color: salmon;
}
```

![before1](https://velog.velcdn.com/images/oigu529/post/8ffe55a9-ba64-4a88-ad75-7f11a36e50b7/image.png)

### z-index 적용 후(1)

```css
.absolute {
  position: absolute;
  right: 20px;
  z-index: 1;
  background-color: salmon;
}
```

![after1](https://velog.velcdn.com/images/oigu529/post/e711df24-ce64-409c-8317-ac9bd0a37bf0/image.png)

> 빼꼼 😗
