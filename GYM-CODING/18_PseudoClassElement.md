# 고급 선택자

---

<br>

## [`:` 가상 클래스 (Pseudo class)](https://developer.mozilla.org/ko/docs/Web/CSS/Pseudo-classes)

선택한 요소가 특정 상황일 때 동작할 수 있도록
`:`(클론)으로 표기

```css
/* 구문 */
selector:pseudo-class {
  property: value;
}
```

```css
/* 사용 예시 */
button:hover {
  color: blue;
}
```

- `:link` 방문 전 링크
- `:visited` 방문한 링크
- `:active` active (ex. 클릭)
- `:hover` 마우스 포인터 올려 놓는 행동
- `:focus` 사용자가 포커스하고 있는 요소 (탭으로 입력칸 이동할 때 보이는)
- `:nth-child` 자식 목록 중 불러올 인덱스
- `:not(selector)` `not(selector)`안에 포함된 요소 제외
  .
  .
  .

> 대표적인 가상 클래스 사용시 LVHA
> `link` ➡️ `visited` ➡️ `hover` ➡️ `active` 순으로 선언 권장
> 실습을 통해 확인해 보자.

<br>

### 색 지정을 통해 확인

```css
a:link {
  color: cyan;
}
a:visited {
  color: red;
}
a:hover {
  color: blue;
  font-weight: 900;
}
fieldset:hover {
  background-color: lightgrey;
  box-shadow: 0 0 20px grey;
}
a:active {
  color: yellow;
}
```

<br>

### LVHA 🆚 AHVL

![](https://velog.velcdn.com/images/oigu529/post/21fa5784-0110-4d41-80fd-e9f84d5acd96/image.png)

![](https://velog.velcdn.com/images/oigu529/post/e091fd7c-f5e9-4ea2-907e-4b5a7a1b0da9/image.png)

> 아직 방문하지 않은 링크 속성`link` → 방문한 링크 속성`visited` → 마우스 오버 시 속성`hover` → 클릭 등 active 시 속성`active`
>
> `LVHA` ➡️ 이 순서로 만들어야 모든 기능이 제 역할을 함

<br>
<br>

## [`::` 가상 요소 (Pseudo element)](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

`::`(이중 클론)으로 표기

```css
/* 구문 */
selector::pseudo-element {
  property: value;
}
```

```css
/* 사용 예시 */
p::first-line {
  color: blue;
  text-transform: uppercase;
}
```

- `::first-letter` 블록 요소에서 텍스트의 첫 글자
- `::first-line` 블록 요소에서 텍스트 첫 라인
- `::before` 특정 요소 앞에 표시하는 것
- `::after` 특정 요소 뒤에 표시하는 것
- `::selection` 선택한 부분(드래그 같이)
  .
  .
  .
