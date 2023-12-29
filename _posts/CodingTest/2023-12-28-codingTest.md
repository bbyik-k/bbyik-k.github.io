---
title: "[Coidng Test] 코딩테스트 준비 / 백준"
excerpt: "코딩테스트 / 백준"

categories:
  - CodingTest
tags:
  - [Coding test, algorithm, nodejs, javascript]

toc: true
toc_sticky: true

date: 2023-12-28
last_modified_at: 2023-12-29
---

😋 Coding Test 준비 / 백준

## 백준 문제 풀이를 시작하며

- 블로그 작성의 목적

  - 추후 코딩테스트를 다시 연습하게 됐을 때, 초기 세팅의 용이함을 위해
  - 문제 풀이를 하며 사용되는 기본 패턴들, 주요 함수들의 정리 용도  
    -> 메모, 노션 등으로 정리도 가능하지만, 블로그 정리 시 텍스트와 코드블럭 병합 정리의 용이
  - 틀린 문제, 막힌 문제 등에 대한 기록
  - 공개된 공간에 업로드 함으로 동기부여

- 코딩테스트 사이트를 선택하는 기준
  - 백준, 프로그래머스, LeetCode 등등 다양한 코딩 사이트 중, 내가 참고하는 강의에서 백준을 사용하기에 선택.
- 코딩테스트 언어 선택 기준
  - Python과 JavaScript 중 많은 고민을 하다 FrontEnd 개발자기에 JS를 선택.
  - 프론트 분야는 JS로만 응시되는 기업들도 다수 존재.

## 백준 nodeJS, JavaScript 기본 입출력 형식

```js
let fs = require("fs");
let input_site = fs.readFileSync("/dev/stdin").toString().split("\n");
let input_local = fs.readFileSync("./data.txt").toString().split("\n");
```

백준 사이트 내에서는 stdin(standard input)을 사용하여 입력값을 받아온다.  
로컬 테스트 시에는 리눅스, 유닉스 운영체제가 아니기에 'data.txt' 파일을 통해 입력값을 받아온다.

추가로 문자열, 단어, 숫자등을 배열로 받아 올 시 공백값 제거를 위해 [filter(Bollean)](#filter) 함수를 이용할 수 있다.

```js
let input = fs
  .readFileSync("/dev/stdin")
  .toString()
  .split("\n")
  .filter(Boolean)
  .map(Number);
```

## 기본 문법 문제 풀이 - 필수 메서드

이전에 c++, python으로만 문제풀이를 몇 번 해보았기에 js 풀이에 익숙해지기 위해 기본 문제들을 풀어보았다. ([soved](https://solved.ac/problems/level) 기준 브론즈~실버 문제)

해결한 문제들은 [Chrome extension](https://chromewebstore.google.com/detail/ccammcjdkpgjmcpijpahlehmapgmphmk?hl=ko&utm_source=ext_sidebar)을 이용하여 자동으로 [Github](https://github.com/bbyik-k/Baekjoon)에 업로드 되도록 해두었다.

![Alt text](https://github.com/bbyik-k/bbyik-k.github.io/assets/47810773/e970e8e5-c1d3-4be3-8a53-4f7171cacd00)

### 필수 메서드 목록

#### filter()

Array 인스턴스의 filter() 메서드는 주어진 배열의 일부에 대한 얕은 복사본을 생성하고, 주어진 배열에서 제공된 함수에 의해 구현된 테스트를 통과한 요소로만 필터링 한다.

배열에서 원하는 값만을 추출하여 새로운 배열을 생성하고 싶을 때 사용.

- 기본 활용

```js
const words = ["spray", "elite", "exuberant", "destruction", "present"];

const result = words.filter((word) => word.length > 6);

console.log(result);
// Expected output: Array ["exuberant", "destruction", "present"]
```

- 문제 풀이 시: input 값 입력 경우

```js
let input = fs
  .readFileSync("/dev/stdin")
  .toString()
  .trim()
  .split(" ")
  .filter(Boolean);
```

이와 같이 input 값 중 유효하지 않은 값(falsy 값)을 필터링 해줄 때 사용 가능하다. 아래와 같은 예시를 들어볼 수 있다.

```js
let arr = [1, 0, "hello", "", true, false, null, undefined];

let filteredArr = arr.filter(Boolean);
console.log(filteredArr);
//output: [1, "hello", true]
```

이는 `filter` 메서드에 `Boolean` 객체를 전달 해준 것으로 다음과 같이 풀어 작성해 볼 수 있다.

```js
let arr = [1, 0, "hello", "", true, false, null, undefined];

let filteredArr = arr.filter(function (element) {
  return Boolean(element);
});

console.log(filteredArr);
```

#### map()

- `map(Number)`

#### Math.max() / Math.fa-minus()

#### split()

#### reduce()

#### Math.floor() / Math.ceil() / Math.round()

- ... spread 연산자

#### indexOf()

#### includes()

#### repeat()

- 문자열 반복

#### 특정 자릿수 반올림 - Number.toFixed()

#### 배열 요소 뒤집기 - reverse()

#### 배열 요소 합치기 - join()
