# ChatGPT 프롬프트 모음

> **만들기 마법사를 쓰면 이 프롬프트를 앱이 자동으로 만들어 줘요.** 인형에 있는 부위에 맞춰 문장이 바뀌고, 카드마다 복사 버튼이 있어요.
> 이 문서는 마법사 없이 직접 만들거나, 프롬프트를 고쳐 쓰고 싶을 때 참고용이에요.

## 사용 방법

1. ChatGPT 새 대화를 열고 **인형 정면 사진**을 첨부해요
2. 아래 프롬프트를 하나씩 보내요. 프롬프트 하나에 이미지 하나예요
3. 같은 대화창에서 이어서 요청하면 색과 질감이 더 잘 맞아요
4. 원본과 다르게 나오면 같은 프롬프트로 다시 만들어서 가장 비슷한 걸 골라요

## 왜 부위를 나눠서 만드나요

동작마다 그림을 통째로 여러 장 만들면 매번 모양과 질감이 조금씩 달라져서 이어 붙였을 때 화면이 떨려 보여요.
몸통, 부위, 표정을 따로 받으면 앱이 팔 흔들기, 걷기, 표정 바꾸기를 코드로 처리해서 원본 느낌 그대로 부드럽게 움직여요.

---

## 공통 문장

모든 이미지 프롬프트(표정 제외) 맨 앞에 들어가요. 아래 프롬프트들에는 이미 들어 있어요.

```
Use the attached photo of my plush toy as the exact reference. Keep the same shape, proportions, colors, fabric texture, stitching and lighting. Do not redesign, simplify or stylize. Front view, camera straight on, centered on a square 1024x1024 canvas. Plain solid pure white background (if the toy itself is white or very light, use a plain solid light green background instead). No shadow, no text, nothing else in the image.
```

---

## 1. body.png: 몸통

따로 움직일 부위를 빼고, 눈과 입만 지운 몸통이에요. **가장 중요한 한 장이에요.**
예시는 귀, 팔, 다리가 있는 인형이에요. 인형에 없는 부위는 문장에서 빼세요.

```
Use the attached photo of my plush toy as the exact reference. Keep the same shape, proportions, colors, fabric texture, stitching and lighting. Do not redesign, simplify or stylize. Front view, camera straight on, centered on a square 1024x1024 canvas. Plain solid pure white background (if the toy itself is white or very light, use a plain solid light green background instead). No shadow, no text, nothing else in the image.

Show the whole toy from the front exactly as in the photo, but remove both ears, both arms, both legs, smoothly filling in the places where they were attached so the body looks complete. Remove only the eyes and the mouth, leaving that area as plain blank fabric. Keep every other feature that does not move, such as a nose, whiskers, blush, patterns, clothes and accessories.
```

따로 움직일 부위가 없는 인형(구름, 공 모양 등)이라면:

```
Use the attached photo of my plush toy as the exact reference. Keep the same shape, proportions, colors, fabric texture, stitching and lighting. Do not redesign, simplify or stylize. Front view, camera straight on, centered on a square 1024x1024 canvas. Plain solid pure white background (if the toy itself is white or very light, use a plain solid light green background instead). No shadow, no text, nothing else in the image.

Show the whole toy from the front exactly as in the photo. Remove only the eyes and the mouth, leaving that area as plain blank fabric. Keep every other feature that does not move, such as a nose, whiskers, blush, patterns, clothes and accessories.
```

> 코, 볼터치, 수염, 무늬, 옷처럼 안 움직이는 건 몸통에 남겨요. 앱이 코를 찾아서 눈은 코 위에, 입은 코 아래에 자동으로 놓아요.

---

## 2. faces.png: 표정 9개

```
Using the attached photo of my plush toy as the reference, create a 3x3 grid of facial expressions for this toy: only the eyes and the mouth (no nose, no blush, no whiskers, no body, no outline of the head), on a plain solid white background. Arrange them in an evenly spaced 3x3 grid, each face centered in its own cell with generous empty space between cells. Every cell uses the same scale and the same eye spacing as the toy's real face, in the same style (for example solid black embroidered eyes with no highlights).
Cells, left to right, top to bottom:
1. neutral: the toy's real expression
2. blink: eyes closed as thin curved lines, same mouth as neutral
3. happy: upside-down U eyes, open smiling mouth
4. talking: normal eyes, small open mouth
5. thinking: eyes looking up and to the right, small wavy mouth
6. sleepy: closed eyes curving downward, tiny round mouth
7. surprised: larger round eyes, small round open mouth
8. pouty: normal eyes, short flat mouth
9. any expression you like
All eyes are exactly the same size in every cell.
```

> 한 장 안에서 아홉 개를 만들어야 서로 스타일이 맞아요. 따로따로 만들지 마세요.

---

## 3. 부위 (있는 것만)

**왼쪽** 한 쪽만 만들어요. 오른쪽은 앱이 좌우를 뒤집어서 써요.

### ear.png: 귀

```
Use the attached photo of my plush toy as the exact reference. Keep the same shape, proportions, colors, fabric texture, stitching and lighting. Do not redesign, simplify or stylize. Front view, camera straight on, centered on a square 1024x1024 canvas. Plain solid pure white background (if the toy itself is white or very light, use a plain solid light green background instead). No shadow, no text, nothing else in the image.

Show only the toy's left ear (the one on the viewer's left) as a single isolated piece, at exactly the same scale as it appears in the front view. Draw its full shape, including the part that is normally hidden where it attaches to the body. Keep it upright, with the base that attaches to the head at the bottom. Isolated on its own, not attached to anything.
```

### arm.png: 팔

```
Use the attached photo of my plush toy as the exact reference. Keep the same shape, proportions, colors, fabric texture, stitching and lighting. Do not redesign, simplify or stylize. Front view, camera straight on, centered on a square 1024x1024 canvas. Plain solid pure white background (if the toy itself is white or very light, use a plain solid light green background instead). No shadow, no text, nothing else in the image.

Show only the toy's left arm (the one on the viewer's left) as a single isolated piece, at exactly the same scale as it appears in the front view. Draw its full shape, including the part that is normally hidden where it attaches to the body. Keep it hanging down naturally along the side of the body, with the shoulder end at the top. Isolated on its own, not attached to anything.
```

### leg.png: 다리

```
Use the attached photo of my plush toy as the exact reference. Keep the same shape, proportions, colors, fabric texture, stitching and lighting. Do not redesign, simplify or stylize. Front view, camera straight on, centered on a square 1024x1024 canvas. Plain solid pure white background (if the toy itself is white or very light, use a plain solid light green background instead). No shadow, no text, nothing else in the image.

Show only the toy's left leg (the one on the viewer's left) as a single isolated piece, at exactly the same scale as it appears in the front view. Draw its full shape, including the part that is normally hidden where it attaches to the body. Keep it upright, with the hip end at the top and the foot at the bottom. Isolated on its own, not attached to anything.
```

### wing.png: 날개, 지느러미

```
Use the attached photo of my plush toy as the exact reference. Keep the same shape, proportions, colors, fabric texture, stitching and lighting. Do not redesign, simplify or stylize. Front view, camera straight on, centered on a square 1024x1024 canvas. Plain solid pure white background (if the toy itself is white or very light, use a plain solid light green background instead). No shadow, no text, nothing else in the image.

Show only the toy's left wing (the one on the viewer's left) as a single isolated piece, at exactly the same scale as it appears in the front view. Draw its full shape, including the part that is normally hidden where it attaches to the body. Keep it in its natural resting position, with the end that attaches to the body at the top right. Isolated on its own, not attached to anything.
```

### tail.png: 꼬리 (하나만)

```
Use the attached photo of my plush toy as the exact reference. Keep the same shape, proportions, colors, fabric texture, stitching and lighting. Do not redesign, simplify or stylize. Front view, camera straight on, centered on a square 1024x1024 canvas. Plain solid pure white background (if the toy itself is white or very light, use a plain solid light green background instead). No shadow, no text, nothing else in the image.

Show only the toy's tail as a single isolated piece, at exactly the same scale as it appears in the photo. Draw its full shape, including the part that is normally hidden where it attaches. The end that attaches to the body on the left side.
```

---

## 잘 안 나올 때

| 문제 | 해결 |
|---|---|
| 배경이 지워지지 않아요 | 배경은 한 가지 색이면 돼요. 흰 인형은 연두색 배경으로 받아요 (공통 문장에 들어 있어요) |
| 인형이 원본과 달라요 | 같은 프롬프트로 다시 만들어서 가장 비슷한 걸 골라요 |
| 질감이 너무 매끈해요 | 끝에 `Visible fabric texture, plush toy photography.` 추가 |
| 팔다리가 몸에 붙어 나와요 | 끝에 `Isolated on its own, not attached to anything.` 추가 (부위 프롬프트에는 이미 들어 있어요) |
| 표정 크기가 들쭉날쭉해요 | 끝에 `All eyes are exactly the same size in every cell.` 추가 (이미 들어 있어요) |
| 표정이 칸 밖으로 넘쳐요 | 끝에 `Each face must fit well inside its cell with generous margins.` 추가 |
