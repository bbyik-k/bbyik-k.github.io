---
title: "[React] Youtube clone coding project"
excerpt: "Youtube cloning 을 통한 React 복습"

categories:
  - React
tags:
  - [React, JavaScript, FrontEnd]

toc: true
toc_sticky: true

date: 2022-05-09
last_modified_at: 2022-05-09
published: false
---

## 검색 기능 리펙토링

- 컴포넌트 내에 네트워크 통신 기능 별도 `class`로 분리
- 소스 내에 보여지는 API Key 분리

  - `'env` 파일 생성하여 분리

- 컴포넌트, View 부분은 최대한 단순하게-> 보여지는 일만 하도록 구성하기
