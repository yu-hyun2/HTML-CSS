# Form 태그

- 사용자의 데이터를 입력받는 양식

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Form 1</title>
  </head>
  <body>
    <form action="">
      <div>
        <label for="username">아이디</label>
        <input type="text" id="username" />
      </div>
      <div>
        <label for="password">비밀번호</label>
        <input type="password" id="password" />
      </div>
      <input type="submit" value="제출하기" />
    </form>
  </body>
</html>
```

![input창](https://velog.velcdn.com/images/oigu529/post/ea05c3b5-f9c8-4590-b644-aa461c7505c9/image.png)

<br>
<br>

# Input 태그

## text

- `<input>` 태그의 기본값
- `type="text"` 일반 텍스트 받음

```html
<input type="text" id="name" />
```

- text 외 다양한 타입 존재(HTML5)
- [MDN `<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)에서 type 확인 가능

<br>

## label `웹 접근성 준수`

<br>

**email** 데이터 받음(이메일 유효성 검증)

```html
<label for="email">이메일</label> <input type="email" id="email" required />
```

![email](https://velog.velcdn.com/images/oigu529/post/f035bf19-a1ea-4d4d-b820-da92c734c712/image.png)

<br>

**required** 를 쓰면 요렇게 필수값이 됨(값 입력 필수)

```html
<label for="text">Text</label> <input type="text" id="text" required />
```

![required](https://velog.velcdn.com/images/oigu529/post/5f23c48f-e0a4-4462-8eed-52baae687e48/image.png)

<br>

## tel

- 모바일로 전화번호 칸 터치하면 숫자 키패드가 올라옴

```html
<label for="tel">전화번호</label> <input type="tel" id="tel" required />
```

<br>

## url

![url](https://velog.velcdn.com/images/oigu529/post/274c4f3f-0259-430e-a0a4-b99b1bfb9949/image.png)

<br>

## number

- min과 max 값을 설정하면 입력 값을 자동으로 유효성 검사
- 범위 안에 들어가지 않으면 오류 메시지

```html
<label for="number">number</label>
<input type="number" id="number" required min="5" max="10" />
```

![number](https://velog.velcdn.com/images/oigu529/post/feabb3c6-3377-446a-baf3-ddb3ffe16f46/image.png)

<br>

## range

![range](https://velog.velcdn.com/images/oigu529/post/a7f4e015-d9f5-4266-8b13-b80467d25861/image.png)

<br>

## date

```html
<label for="date">date</label>
<input type="date" id="date" min="2023-12-18" max="2023-12-31" />
```

![date](https://velog.velcdn.com/images/oigu529/post/88dce98f-ce44-4bde-8167-6b1b47507513/image.png)

- 18~31 선택할 수 있는 범위가 지정된 것을 확인할 수 있음

<br>

## time

- 시간 범위 설정하면 선택은 가능하지만, email처럼 제출 시 유효성 체크

```html
<label for="time">time</label>
<input type="time" id="time" min="09:00" max="18:00" />
```

![time](https://velog.velcdn.com/images/oigu529/post/5deda076-75d5-469e-9c66-1d45a0b71d51/image.png)

<br>

## password

- ●●●● 마스킹 처리 되어 표시

```html
<label for="password">password</label>
<input type="password" id="password" required />
```

![password](image.png)

<br>

### label

### checkbox

### radio

### number

### range

### 날짜/시간

### hidden

- 서버 측으로 어떠한 데이터를 넘길 때 사용

### file

### image

### button

---

### fieldset

- 데이터 그룹화 가능

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Form Input</title>
  </head>
  <body>
    <form action="">
      <fieldset>
        <legend>개인정보</legend>
        <input type="text" />
        <input type="text" />
      </fieldset>
      <fieldset>
        <legend>사업자정보</legend>
        <input type="text" />
        <input type="text" />
      </fieldset>

      <input type="text" />
      <input type="text" />
    </form>
  </body>
</html>
```

![fieldset-ex](https://velog.velcdn.com/images/oigu529/post/2fb5f59c-fc78-4c7a-8c80-f7acca49c086/image.png)

<br>

### legend

<br>

## textarea, select, button

<br>
