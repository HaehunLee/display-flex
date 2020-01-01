# display : flex;

## * Container / Items
```
Container : items를 감싸는 부모 요소.
(Items를 정렬하기 위해 Container가 필수임.)
```

## * 속성
```
Container : flex, flex-flow, justify-content 등...
Items : order, flex, align-self 등...
```

## * Flex Container ([CodePen](https://codepen.io/haehunlee/pen/Baywxrv))
```css
display : flex;
    /* Container가 block 효과를 받게됨. */
display : inline-flex;
    /* flex와 같은 효과지만, Container가 inline효과를 받게된다. */
```

---

<ol>

### 1. flex-flow
```css
flex-flow : 주축 여러줄묶음; 
/*밑의 속성의 단축 속성*/
```

<table>

| 값 | 의미 | 기본값 |
|---|:---:|---:|
|`flex-direction`|items의 주 축(main-axis)를 설정|`row`
|`flex-wrap`|items의 여러 줄 묶음(줄 바꿈) 설정|`nowrap`

</table>

#### - flex-direction

`flex-direction : 주축;`
- Items의 주 축(maxin-axis)을 설정합니다.

<table>

| 값 | 의미 | 기본값 |
|---|:---:|---:|
|`row`|items를 수평축(왼쪽에서 오른쪽)으로 표시|`row`
|`row-reverser`|items를 row의 반대 축으로 표시|
|`column`|items를 수직축(위에서 아래로) 표시|
|`column-reverse`|items를 column의 반대 축으로 표시|

</table>

---

#### - flex-wrap ([CodePen](https://codepen.io/haehunlee/pen/XWJeqBj))
- Items의 여러 줄 묶음(줄 바꿈)을 설정합니다.

<table>

| 값 | 의미 | 기본값 |
|---|:---:|---:|
|`nowrap`|모든 Items를 여러 줄로 묶지 않음(한 줄에 표시)|`nowrap`
|`wrap`|Items를 여러 줄로 묶음|
|`wrap-reverse`|Items를 wrap의 역방향으로 여러 줄로 묶음

</table>

---

### 2. justify-content ([CodePen](https://codepen.io/haehunlee/pen/eYmGrPZ))
`justify-content : 정렬방법;`
```
- 주 축(main-axis)의 정렬 방법을 설정합니다.
```

<table>

| 값 | 의미 | 기본값 |
|---|:---:|---:|
|`flex-start`|items를 시작점(flex-start)으로 정렬|`flex-start`
|`flex-end`|items를 끝점(flex-end)으로 정렬|
|`center`|items를 가운데 정렬|
|`space-between`|시작 item은 시작점에,<br> 마지막 item은 끝점에 정렬되고,<br> 나머지 items는 사이에 고르게 정렬된다.|
|`space-around`|items를 균등한 여백을 포함하여 정렬|

</table>

---

### 3. align-content ([CodePen](https://codepen.io/haehunlee/pen/LYEzmXO))

`align-content : 정렬방법;`

```
- 교차 축(cross-axis) 정렬 방법을 설정합니다.
- flex-wrap으로 items가 여러 줄이고, 여백이 있을 경우만 사용할 수 있다.
- items가 한 줄일 경우 align-items 속성을 사용한다.
```

<table>

| 값 | 의미 | 기본값 |
|---|:---:|---:|
|`stretch`|Container의 교차 축을 채우기 위해<br> items를 늘림|`stretch`
|`flex-start`|items를 시작점(flex-start)으로 정렬|
|`flex-end`|items를 끝점(flex-end)으로 정렬|
|`center`|items를 가운데 정렬|
|`space-between`|시작 item은 시작점에,<br> 마지막 item은 끝점에 정렬되고,<br> 나머지 items는 사이에 고르게 정렬된다.|
|`space-around`|items를 균등한 여백을 포함하여 정렬|

</table>

---

### 4. align-items ([CodePen](https://codepen.io/haehunlee/pen/RwNLJNq))
```
- 교차 축(cross-axis) 정렬 방법을 설정한다.
- items가 한 줄일 경우 많이 사용한다.
- 여러 줄일 경우 align-content 속성이 우선이 된다.
- align-items를 사용하려면, align-content를 기본값(stretch)설정해야 한다.
```

<table>

| 값 | 의미 | 기본값 |
|---|:---:|---:|
|`stretch`|Container의 교차 축을 채우기 위해<br> items를 늘림|`stretch`
|`flex-start`|items를 시작점(flex-start)으로 정렬|
|`flex-end`|items를 끝점(flex-end)으로 정렬|
|`center`|items를 가운데 정렬|
|`baseline`|items를 문자기준선에 정렬|

</table>

</ol>


<hr>


## * Flex Items
```
- Flex Items를 위한 속성
```

<table>

| 값 | 의미 |
|---|:---:|
|`order`|Flex Items의 순서를 설정|
|`flex`|`flex-grow`, `flex-shrink`, `flex-basis`의 단축 속성|
|`flex-grow`|Flex Item의 증가 너비 비율을 설정|
|`flex-shrink`|Flex Item의 감소 너비 비율을 설정|
|`flex-basis`|Flex Item의 (공간 배분 전) 기본 너비 설정|
|`align-self`|교차 축(cross-axis)에서 Item의 정렬 방법을 설정|

</table>

---

<ol>

### 1. order ([CodePen](https://codepen.io/haehunlee/pen/bGNoKVb))
`order : 순서;`
```
- Item의 순서를 정한다.
- Item에 숫자를 지정하고, 숫자가 클수록 순서가 밀린다.
- 음수가 허용된다.
```

<table>

| 값 | 의미 | 기본값 |
|---|:---:|:---:|
|숫자|`item`의 순서를 결정|0

</table>

---

### 2. flex-grow ([CodePen](https://codepen.io/haehunlee/pen/wvBrXMw))
`flex-grow : 증가너비;`
```
- Item의 증가 너비 비율을 설정한다.
- 숫자가 크면 더 많은 너비를 가진다.
- Item이 가변 너비가 아니거나, 값이 0일 경우 효과가 없다.
```
<table>

| 값 | 의미 | 기본값 |
|---|:---:|:---:|
|숫자|`item`의 증가 너비 비율을 설정|0

</table>

---

### 3. flex-shrink
`flex-shrink : 감소너비;`
```
- Item이 감소하는 너비의 비율을 설정한다.
- 숫자가 크면 더 많은 너비가 감소한다.
- Item이 가변 너비가 아니거나, 값이 0일 경우 효과가 없다.
```

<table>

| 값 | 의미 | 기본값 |
|---|:---:|:---:|
|숫자|`item`의 감소 너비 비율을 설정|1

</table>

---

### 4. flex-basis
`flex-basis : 기본너비;`
```
- Item의 (공간 배분 전) 기본 너비를 설정한다.
- 값이 auto일 경우 width, height 등의 속성으로 Item의 너비를 설정할 수 있다.
- 단위 값이 주어질 경우 설정할 수 없다.
```
<table>

| 값 | 의미 | 기본값 |
|---|:---:|:---:|
|`auto`|가변 `item`과 같은 너비|`auto`
|단위|px, em, cm 등 단위로 지정|

</table>

---

### 5. flex ([CodePen](https://codepen.io/haehunlee/pen/gObGKWN))
`flex : 증가너비 감소너비 기본너비;`

```css
.item {
    flex : 1 1 20px;  /* 증가너비 : 1, 감소너비 : 1, 기본너비 : 20px */
    flex : 1 11; 
    /* 증가너비 : 1, 감소너비 : 1, 
    (명시되지 않은 flex-basis의 기본값은 auto가 아닌, 
    0이 되어 버린다.) */
}
```

```
- Item의 너비(증가, 감소, 기본)를 설정하는 단축 속성입니다.
```
<table>

| 값 | 의미 | 기본값 |
|---|:---:|:---:|
|`flex-grow`|`item`의 증가 너비 비율을 설정|0
|`flex-shrink`|`item`의 감소 너비 비율을 설정|1
|`flex-basis`|`item`의 (공간 배분 전) 기본 너비 설정|`auto`

</table>

---

### 6. align-self

```
- 교차 축(cross-axis)에서 개별 Item의 정렬 방법를 설정한다.

- align-items는 Container 내 모든 Items의 
  정렬 방법을 설정한다.

- 필요에 의해 일부 Item만 정렬 방법을 변경하려고 할 경우 
  align-self을 사용할 수 있다. 이 속성은 
  align-items 속성보다 우선시 된다.
```
<table>

| 값 | 의미 | 기본값 |
|---|:---:|:---:|
|`auto`|Container의 `align-items` 속성을 상속받음|`auto`
|`stretch`|Container의 교차 축을 채우기 위해 `item`을 늘림|
|`flex-start`|`item`을 각 줄의 시작점(`flex-start`)으로 정렬|
|`flex-end`|`item`을 각 줄의 끝점(flex-end)으로 정렬|
|`center`|`item`을 가운데 정렬|
|`baseline`|`item`을 문자기준선에 정렬|

</table>

</ol>

---