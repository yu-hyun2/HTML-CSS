> ### 참고한 사이트
>
> - 강의 [짐코딩 유튜브 ](https://www.youtube.com/watch?v=nmCh-6iHHQI&list=PLlaP-jSd-nK-ponbKDjrSn3BQG9MgHSKv&index=28)
> - 사진 [pixabay1](https://pixabay.com/ko/photos/%EC%97%AC%EC%9A%B0-%EC%9E%90%EC%97%B0-%EB%8F%99%EB%AC%BC-%EB%A3%A8-%EB%8F%99%EB%AC%BC%EA%B5%B0-5042242/) [pixabay2](https://pixabay.com/ko/photos/%EC%97%AC%EC%9A%B0-%EB%B6%89%EC%9D%80-%EC%97%AC%EC%9A%B0-%EB%8F%99%EB%AC%BC-%EC%9E%90%EC%97%B0-5064828/),
> - 글 [위키백과](https://ko.wikipedia.org/wiki/%EC%97%AC%EC%9A%B0)
>
> 오늘은 귀여운 여우로 실습 !~!

<br>
<br>

# ✔️ float 속성

---

인접한 텍스트나 인라인 요소가 주위를 자연스럽게 감싸게 함

- `none` 기본값, 요소를 띄우지 않음
- `left` 왼쪽에 띄움
- `right` 오른쪽에 띄움
- `inherit` 부모 요소로부터 상속
- `initial` 기본값으로 설정

<br>

## 실습

1. display `block` 요소인 `div` 태그로 container를 만들고 그 안에 `p` 문단 블록 태그를 사용해서 이미지와 글을 넣었다.

```html
<!-- html -->
<div class="container">
  <p>
    <img class="float-left" src="../image/15_fox1.jpg" alt="fox1" />
    여우는 개과에 속하는 여러 동물의 총칭이다. 개과의 동물 중 작은 편에 속하는
    동물로, 보통의 개보다 작으며 ~~~
  </p>
  <p>
    <img class="float-right" src="../image/15_fox2.jpg" alt="fox2" />
    여우는 잡식성 동물이다.~~~
  </p>
</div>
```

<br>
  
2. container와 img의 너비를 설정하고 container는 회색 박스까지 만듦
  ```css
  /* css */
  .container {
    width: 800px;
    border: 1px solid gray;
  }

img {
width: 200px;
}

````
![before](https://velog.velcdn.com/images/oigu529/post/3d54ec79-a9c2-49cf-a405-b2860dd5e294/image.png)


3. 각 사진에 `float-left`, `float-right` 설정하고 글씨 10px만큼 사진에서 떨어져...
```css
/* css */
.float-left {
  float: left;
  margin-right: 10px;
}

.float-right {
  float: right;
  margin-left: 10px;
}

p {
  border: 1px solid blue;
}
````

![p](https://velog.velcdn.com/images/oigu529/post/1fdffe6d-5afa-40a6-9e66-c72e29fedffa/image.png)

- 텍스트가 아주 예쁘게 사진 옆으로 옮겨붙은 것을 볼 수 있음 ^0^0^
  저기 텍스트 밑에 삐져나온 게 맘에 들지 않는다면 컨테이너의 `width`를 넓히면 돼 ~ !요 ~ !
  ![width](https://velog.velcdn.com/images/oigu529/post/7b14c1af-f2b1-4821-92d0-3cb18a63921b/image.png)
- `.container` `width` 800px에서 1200px까지 늘림
- 또 여기서 저기 두 번째 문단 시작할 때 첫 번째 문단이랑 구분하고 싶고... 쟤랑 좀 떨어지고 싶으면 그 때 사용하는 게 `clear`!!!!!!!!!!!!!!!!!!!!

<br>
<br>

# ✔️ clear 속성

---

float 속성을 취소함

- `clear: none;` 기본값
- `clear: left;` 왼쪽 취소
- `clear: right;` 오른쪽 취소
- `clear: both; ` 둘다 취소

<br>

## 실습

4. 자 이렇게 clear를 사용해서 p태그의 float 속성을 취소했다.
   ![](https://velog.velcdn.com/images/oigu529/post/8cea9000-d66a-49e7-b368-48a82cae4edb/image.png)
   코드를 어떻게 작성할까? ➡️ float이랑 사용 방법이 같다. 근데 속성값은 none left right 외 다른 게 있음 주의

```css
/* css */
.clear {
  clear: both;
}
```

이렇게 `css`에서 설정하고 `html`에서 적용하면 첫 번째 문단 이미지의 `float` 속성에 걸리지 않는다 ~

> 그런데 또 저렇게 첫 번째 이미지랑 두 번째 문단이 붙어있는 게 맘에 안 들어?
> 그럼 `br`태그를 사용하든가 아니면 `float-left`의 `css` 속성에서 `margin-bottom: 20px;`로 설정해 버린다.

<br>

### `<br>` 적용

![br](https://velog.velcdn.com/images/oigu529/post/cbb56653-89d9-4449-8532-ca249b65967f/image.png)

<br>

### `margin-bottom: 20px;` 적용

![bottom](https://velog.velcdn.com/images/oigu529/post/199e2f0c-e48c-4405-865f-d0b6e4362417/image.png)

이렇게 우리가 원하는 이상적인 ~ 간격 ~ 완성 ~!

 <br>

> 내가 한 실습에서 이미지가 두 개뿐이라서 `br`을 쓰거나 `float-left`에 bottom 간격을 조절한 거지만 만약 문단이 많아지면 유지보수가 어렵지 않을까........
> ➡️ p태그에서 margin-bottom과 margin-top 간격을 조정하는 게 좋은 방법일 것 같다.

1. `bottom`만 100px
   ![](https://velog.velcdn.com/images/oigu529/post/47ab0f94-5c4e-4dbd-9d96-7bef32c5c5fa/image.png)

2. `top`과 `bottom` 둘다 50px씩
   ![](https://velog.velcdn.com/images/oigu529/post/38aa82e9-382a-478b-ab62-a2daf76f1869/image.png)

> 두 번째 top과 bottom을 같이 조정하는 게 예쁘죠 ~^^
