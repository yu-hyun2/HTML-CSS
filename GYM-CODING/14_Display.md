# Block

대표적인 Block element인 `div`와 `h2`로 실습

```html
<h1>Display Block</h1>
<!-- Block element -->
<div>content</div>
<div>content</div>
<div>content</div>
<!-- Block element -->
<h2>title</h2>
```

![displayblock](https://velog.velcdn.com/images/oigu529/post/8afedd3e-684f-45ab-b294-938af9bfe667/image.png)

실행하면 `display` 기본값이 `block`으로 되어있음을 확인할 수 있음

<br>

# Inline

`width`와 `height`가 적용되지 않음

```css
div,
h2 {
  border: 1px solid grey;
  width: 100px;
  height: 100px;
}

span,
a {
  border: 1px solid blue;
  width: 100px;
  height: 100px;
}
```

- ![displayinline](https://velog.velcdn.com/images/oigu529/post/99d2893a-acc5-47a8-852d-d37de56079b3/image.png)

<br>

# None

`display: none;`과 `visibility: hidden;`의 차이

- **`visibility: hidden;`**

- ![visibility](https://velog.velcdn.com/images/oigu529/post/aa01519c-27b5-410c-b8f3-135947c6434a/image.png)

- **`display: none;`**
- ![displaynone](https://velog.velcdn.com/images/oigu529/post/bbe9c1b6-a260-4795-b0bc-f286227097b1/image.png)

<br>

# Inline-Block

block태그 `div`와 inline태그 `span`을 같이 작성하고

```html
<article>
  <h1>Display Inline Block</h1>
  <div>content</div>
  <div>content</div>
  <div>content</div>
  <span>content</span>
  <span>content</span>
  <span>content</span>
</article>
```

- ![article](https://velog.velcdn.com/images/oigu529/post/12c4cdc9-36ab-4c69-acc1-00b3cc4a9132/image.png)

여기에 css display 설정을 `inline-block`으로 하면 .!!!!

```css
article > div,
article > span {
  display: inline-block;
}
```

- ![inline-block](https://velog.velcdn.com/images/oigu529/post/13ffde0e-2de9-4aea-a84f-31582b151f66/image.png)

이렇게 보면 그냥 inline 형태 같지만? `width`와 `height`를 적용해 보자.

- ![inline-block2](https://velog.velcdn.com/images/oigu529/post/51025f4b-bb6f-44b4-956f-e596f968e726/image.png)

> inline에서는 안 되는 `width`, `height` 조절이 가능한 것을 확인할 수 있다 !

<br>
<br>

## 😀 메뉴 상단바 제작 ! ! !

![menu](https://velog.velcdn.com/images/oigu529/post/412cce4c-56e0-4d1f-b819-4dceffd528ba/image.png)

### html

메뉴에 들어갈 글자를 html에서 리스트 형태로 만들고

```html
<nav>
  <ul>
    <li><a href="#" class="active">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
    <li><a href="#">Feedback</a></li>
  </ul>
</nav>
```

### css

css 설정을 이렇게 했다.

```css
* {
  padding: 0;
  margin: 0;
  text-decoration: none;
  list-style: none;
}
nav {
  background-color: #34495e;
  width: 100%;
  height: 80px;
}
nav li {
  display: inline-block;
  margin: 8px;
  line-height: 50px;
}
nav a {
  color: white;
  font-size: 20px;
  text-transform: uppercase; /* 모두 대문자로 변경 */
}
a.active,
a:hover {
  border: 1px solid white;
}
```

### 하나씩 봅시다 ~

1. `*`는 전체 선택자로 속성을 초기화할 때 쓰기 좋다 !
   padding, margin, 스타일 등을 초기화했다.

2. `nav` 태그는 navigation의 줄임말로 문서 내에서 링크를 그룹화할 때 사용한다고 한다! 지금 메뉴바를 만들기 때문에 이 메뉴 링크를 담을 수 있는 `nav`로 `ul`>`li` 목록들을 그룹지었다.

3. `nav`의 자식태그인 `a`태그를 흰색, 20px, 대문자로 변경해준다.

4. `a`태그의 클래스인 `active`와 `a`태그를 마우스 오버했을 때 하얀 박스가 표시될 수 있도록 한다.
