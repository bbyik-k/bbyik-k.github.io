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
last_modified_at: 2023-12-28
---

😋 Coding Test 준비 / 백준

## 백준 문제 풀이를 시작하며

---

- 코딩테스트 사이트를 선택하는 기준  
  백준, 프로그래머스, LeetCode 등등 다양한 코딩 사이트 중, 내가 참고하는 강의에서 백준을 사용하기에 선택하였다.
- 코딩테스트 언어 선택 기준  
  Python과 JavaScript 중 많은 고민을 하다 FrontEnd 개발자기에 JS를 선택.  
  프론트 분야는 JS로만 응시되는 기업들도 다수 존재.

## 백준 nodeJS, JavaScript 기본 입출력 형식

```js
let fs = require("fs");
let input_site = fs.readFileSync("/dev/stdin").toString().split("\n");
let input_local = fs.readFileSync("./data.txt").toString().split("\n");
```

백준 사이트 내에서는 stdin(standard input)을 사용하여 입력값을 받아온다.  
로컬 테스트 시에는 리눅스, 유닉스 운영체제가 아니기에 'data.txt' 파일을 통해 입력값을 받아온다.
