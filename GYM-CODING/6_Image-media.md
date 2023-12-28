### 절대경로

- http~, /~
- 절대적인 고유한 경로 지정
- `root directory` C:\ 같은 최상위 폴더 이름

### 상대경로

- ./ ../
- 현재 문서를 기준으로 경로 지정
- 상위 폴더인 A의 하위 폴더인 image에 파일이 있는 경우
  `"A/image/6_snowman.jpg"`
  `"A/현재 문서"`
- 현재 문서보다 상위인 폴더는 ..으로 표시
  `"../image/6_snowman.jpg"`

---

## 이미지 태그 `<img>`

```html
<img src="image/snowman.jpg" alt="눈사람" />
```

- `src`는 필수 사항이며 이미지 경로를 나타냄
- `alt`는 선택 사항이며 이미지를 설명하는 텍스트
- 이미지를 불러올 수 없을 때 `alt` 내용을 표시

![alt 표시 확인](https://velog.velcdn.com/images/oigu529/post/d1304a99-bc54-425f-a2b6-3076b296df9f/image.png)

⭐ 현재 폴더의 상위 폴더를 불러올 때는 ../을 사용함..

```html
<img src="../image/6_snowman.jpg" alt="눈사람" />
```

이렇게 ^0^

<br>

## 오디오 태그 `<audio>`

- 소리 콘텐츠
- src 속성 or `<source>` Element를 사용해 한 개 이상의 오디오 소스 지정 가능

```html
<!-- src -->
<audio src="../media/audio.mp3" controls></audio>

<!-- source Element -->
<audio controls>
  <source src="Audio.mp3" type="audio/mp3" />
  <source src="Audio.ogg" type="audio/ogg" />
</audio>
```

![pixabay](https://velog.velcdn.com/images/oigu529/post/b8108b54-d4ce-4253-af46-8774a6cbb518/image.png)

- controls를 하지 않으면 컨트롤 바가 나오지 않음

<br>

## 비디오 태그 `<video>`

```html
<h2>비디오 태그</h2>
<video
  width="400"
  src="../media/video.mp4"
  type="video/mp4"
  poster="../image/6_poster.jpg"
  controls
></video>
```

- poster는 썸네일에 들어갈 이미지

![videvo](https://velog.velcdn.com/images/oigu529/post/025881f9-aadb-4ed0-accb-9724f5cc7cc9/image.png)

- controls를 하지 않으면 컨트롤 바가 나오지 않음

<br>

## 하이퍼링크 `<a>` ⭐

- 외부 링크로 연결

```html
<!-- 하이퍼링크 -->
<a href="연결할 링크">표시할 이름</a>

<!-- 새 탭으로 링크 열기 -->
<a href="연결할 링크" target="_blank">
  <!-- 바로 메일 보낼 수 있게 -->
  <a href="mailto:bruce.이메일주소@mail.com">표시할 이름</a>

  <!-- 현재 페이지에서 지정한 target으로 이동 -->
  <a href="#target">25로 이동</a></a
>
```
