> 참고한[ GYM CODING 유튜브](https://www.youtube.com/watch?v=XmBwKeoveFA&list=PLlaP-jSd-nK-ponbKDjrSn3BQG9MgHSKv&index=24)
> 참고한[ GYM CODING 노션](https://www.gymcoding.co/c58de03a-0f9a-40b8-90bd-7951ae27d606#5a71bbfa-0dcd-4c51-bfbe-814c98364897)

<br>

# 구성

---

![boxmodel구성](https://velog.velcdn.com/images/oigu529/post/b983f46d-f24f-4ec9-bf9f-82ec30fb603c/image.png)

Inline Level Element에는 width, height이 적용되지 않음

[Display-value 참고](https://velog.io/@oigu529/gym-html-css5)

<br>

## inline-block 설정 전

```css
span {
  border: 1px solid red;
  width: 100px;
  height: 100px;
}
```

![display before](https://velog.velcdn.com/images/oigu529/post/7b9a2642-6aad-42a9-8af1-8f3edf4bb225/image.png)

<br>

## inline-block 설정 후

```css
span {
  border: 1px solid red;
  width: 100px;
  height: 100px;
  display: inline-block;
}
```

![display after](https://velog.velcdn.com/images/oigu529/post/79a87d7c-33ad-42e0-a1b3-6cc48ef1b8ed/image.png)

> ### ⭐ `inline-block`

- **`block`**과 **`inline`**의 중간 형태
- 요소는 inline인데 내부는 block처럼 표시

<br>
<br>

# margin

---

### margin 중첩 현상

![중첩](https://velog.velcdn.com/images/oigu529/post/2d7c44a1-8070-4d9a-b987-2b53ac4c0c6f/image.png)

거리가 40px이어야 하는데 중첩 현상 때문에 20px만 떨어져 있는 것을 확인할 수 있음

<br>

![중첩보완](https://velog.velcdn.com/images/oigu529/post/ca40f900-c7b7-4c75-a2ae-9cf752aba597/image.png)

```html
<div class="shape" style="margin-bottom: 40px"></div>
<div class="shape"></div>
```

인라인으로 지정하게 되면 우선순위가 인라인 먼저이기 때문에 40px로 지정됨

<br>
<br>

# border

---

```css
.border {
  width: 200px;
  height: 200px;
  border: 1px solid black;
  border-top: 10px dotted red;
  border-bottom: 5px dashed blue;
  border-left: 1px solid yellow;
  border-right: 3px solid cyan;
}
```

![border1](https://velog.velcdn.com/images/oigu529/post/3e353cc4-e606-445d-bedd-032323697b08/image.png)

`border-radius: 20%;`와 `border-radius: 50%;` 차이
![20 or 50](https://velog.velcdn.com/images/oigu529/post/b5ee78bf-021e-4b5d-ae39-4eef7a45e201/image.png)

<br>

### 💡 content-box vs border-box

```css
.content-box {
  width: 100px;
  height: 100px;
  border: 10px solid blue;
  padding: 20px;
  margin: 10px;
  box-sizing: content-box;
}
.border-box {
  width: 100px;
  height: 100px;
  border: 10px solid red;
  padding: 20px;
  margin: 10px;
  box-sizing: border-box;
}
```

![content-box](https://velog.velcdn.com/images/oigu529/post/9454b2e4-1349-4bdb-bd3c-597f78adfa7c/image.png)

![border-box](https://velog.velcdn.com/images/oigu529/post/a7c2aeb7-6d0a-4ab5-9636-e7c3e2ba2b35/image.png)

`content-box` 포함되지 않은 사이즈
`border-box` 포함된 사이즈
