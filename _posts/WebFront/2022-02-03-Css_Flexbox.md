---
title: "[CSS] Flexbox"
excerpt: "Flexbox Froggy 게임을 통한 CSS 학습"

categories:
  - CSS
tags:
  - [CSS, Html, FrontEnd]

toc: true
toc_sticky: true

date: 2022-02-03
last_modified_at: 2022-02-03
---

## Flexbox Froggy

- Site Link  
  https://flexboxfroggy.com/#ko

### 1~4단계: **_`justify-content`_**

- **기준**선상에서의 정렬

1. `flex-start`: 요소들을 컨테이너의 왼쪽으로 정렬합니다.
2. `flex-end`: 요소들을 컨테이너의 오른쪽으로 정렬합니다.
3. `center`: 요소들을 컨테이너의 가운데로 정렬합니다.
4. `space-between`: 요소들 사이에 동일한 간격을 둡니다.
5. `space-around`: 요소들 주위에 동일한 간격을 둡니다.

### 5~7단계: **_`align-items`_**

- **기준축의 반대**선상에서의 정렬

1. `flex-start`: 요소들을 컨테이너의 꼭대기로 정렬합니다.
2. `flex-end`: 요소들을 컨테이너의 바닥으로 정렬합니다.
3. `center`: 요소들을 컨테이너의 세로선 상의 가운데로 정렬합니다.
4. `baseline`: 요소들을 컨테이너의 시작 위치에 정렬합니다.
5. `stretch`: 요소들을 컨테이너에 맞도록 늘립니다.

### 8~13단계: **_`flex-direction`_**

- 정렬 축 방향 설정

1. `row`: 요소들을 텍스트의 방향과 동일하게 정렬합니다.
1. `row-reverse`: 요소들을 텍스트의 반대 방향으로 정렬합니다.
1. `column`: 요소들을 위에서 아래로 정렬합니다.
1. `column-reverse`: 요소들을 아래에서 위로 정렬합니다.

### 14~15단계: **_`order`_**

- 아이템 각 요소 순서 변경
- z-index 같은 속성으로 낮은 값이 앞으로 배치

1. `기본 값은 0
1. `양수 혹은 음수로 변경 가능

### 16~17단계: **_`align-self`_**

- 개별 요소에 적용할 수 있는 align-items 속성
- align-items 에서 사용하는 값들 인자로 받음

1. `flex-start`: 요소들을 컨테이너의 꼭대기로 정렬합니다.
2. `flex-end`: 요소들을 컨테이너의 바닥으로 정렬합니다.
3. `center`: 요소들을 컨테이너의 세로선 상의 가운데로 정렬합니다.
4. `baseline`: 요소들을 컨테이너의 시작 위치에 정렬합니다.
5. `stretch`: 요소들을 컨테이너에 맞도록 늘립니다.

### 18~19단계: **_`flex-wrap`_**

- 요소 줄 변경 설정

1. `nowrap`: 모든 요소들을 한 줄에 정렬합니다.
1. `wrap`: 요소들을 여러 줄에 걸쳐 정렬합니다.
1. `wrap-reverse`: 요소들을 여러 줄에 걸쳐 반대로 정렬합니다.

### 20단계: **_`flex-flow`_**

- `flex-direction` + `flex-wrap` 함께 사용 가능

1. ex) flex-flow: column wrap;
1. ex) flex-flow: row wrap;

### 21~23단계: **_`align-content`_**

- 여러 줄 사이의 간격을 지정
- `align-content`는 여러 줄들 사이의 간격을 지정하며,  
  `align-items`는 컨테이너 안에서 어떻게 모든 요소들이 정렬하는지를 지정.  
  한 줄만 있는 경우, `align-content` 는 효과를 보이지 않습니다.

1. `flex-start`: 여러 줄들을 컨테이너의 꼭대기에 정렬합니다.
1. `flex-end`: 여러 줄들을 컨테이너의 바닥에 정렬합니다.
1. `center`: 여러 줄들을 세로선 상의 가운데에 정렬합니다.
1. `space-between`: 여러 줄들 사이에 동일한 간격을 둡니다.
1. `space-around`: 여러 줄들 주위에 동일한 간격을 둡니다.
1. `stretch`: 여러 줄들을 컨테이너에 맞도록 늘립니다.

### 24단계: 종합 문제

성공

```CSS
#pond {
  display: flex;
  flex-direction: column-reverse;
  flex-wrap: wrap-reverse;
  justify-content: center;
  align-content: space-between;
}
```
