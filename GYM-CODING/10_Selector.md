# CSS 선택자

---

## 기본 선택자

```css
/* *은 전체 선택을 의미 (전체 선택자) */
* {
  margin: 0;
  padding: 0;
}

/* 태그명이 h1인 요소 선택 (타입 선택자) */
h1 {
  color: blue;
}

/* class에 title을 갖는 모든 요소 선택(클래스 선택자) */
/* ex)) <h1 class="title"> */

.title {
  color: blue;
}
```

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Selector Basic</title>
    <style>
      /* * {
        margin: 0;
        padding: 0;
      } */
      h2 {
        color: green;
      }
      p {
        color: grey;
        font-weight: 400;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <h1>애국가</h1>
    <hr />
    <h2>1</h2>
    <p>
      동해 물과 백두산이 마르고 닳도록<br />
      하느님이 보우하사 우리나라 만세<br />
      무궁화 삼천리 화려강산<br />
      대한 사람 대한으로 길이 보전하세
    </p>

    <h2>2</h2>
    <p>
      남산 위에 저 소나무 철갑을 두른 듯<br />
      바람 서리 불변함은 우리 기상일세<br />
      무궁화 삼천리 화려강산<br />
      대한 사람 대한으로 길이 보전하세
    </p>

    <h2>3</h2>
    <p>
      가을 하늘 공활한데 높고 구름 없이<br />
      밝은 달은 우리 가슴 일편단심일세<br />
      무궁화 삼천리 화려강산<br />
      대한 사람 대한으로 길이 보전하세
    </p>

    <h2>4</h2>
    <p>
      이 기상과 이 맘으로 충성을 다하여<br />
      괴로우나 즐거우나 나라 사랑하세<br />
      무궁화 삼천리 화려강산<br />
      대한 사람 대한으로 길이 보전하세
    </p>
  </body>
</html>
```

![statement style](https://velog.velcdn.com/images/oigu529/post/148b6ada-9482-4fe0-96e3-546ac22fbdbb/image.png)

<br>

## ✔️ Class 선택자

- 중복으로 작성 가능

```html
<style>
  /* Class 선택자 */
  .red--text {
    color: red;
  }
  .blue--text {
    color: blue;
  }
</style>
```

![class selector](https://velog.velcdn.com/images/oigu529/post/77235298-7c0f-471f-a579-b1bceeb18d57/image.png)

<br>

## ✔️ ID 선택자

- 고유한 하나의 태그에만 사용 ➡️ 웹 표준

<br>
