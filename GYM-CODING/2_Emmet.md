# Emmet

### 자식노드 `>`

- 자식 요소 생성
- `div>ul>li Tab`

```html
<div>
  <ul>
    <li></li>
  </ul>
</div>
```

<br>

### 형제노드 `+`

- 한 요소와 같은 단계에 위치한 요소 생성
- `div>ul+ol+div Tab`

```html
<div>
  <ul></ul>
  <ol></ol>
  <div></div>
</div>
```

<br>

### 반복하기 `*`

- 요소를 반복해 생성
- `div>ul>li*3 Tab`

```html
<div>
  <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul>
</div>
```

<br>

### 아이디 `#`

- id를 갖는 요소 생성(기본이 div이기 때문에 생략 가능)
- `span#item Tab`
- `#item Tab`

```html
<div id="item"></div>
<span id="item"></span>
```

<br>

### 클래스 `.`

- CSS 클래스를 가질 요소 생성(기본이 div이기 때문에 생략 가능)
- `span.title Tab`
- `.title Tab`

```html
<span class="title"></span>
<div class="title"></div>
```

<br>

### 콘텐츠(텍스트 입력) `{}`

- 요소 안에 내용을 갖는 요소 생성
- `p.container{Hello World~!} Tab`

```html
<p class="container">Hello World~!</p>
```

<br>

### 자동 넘버링 부여 `$`

- 넘버링 부여
- `p.container{item$} Tab`

```html
<!-- p.container{item$}*5 Tab -->
<p class="container">item1</p>
<p class="container">item2</p>
<p class="container">item3</p>
<p class="container">item4</p>
<p class="container">item5</p>
```
