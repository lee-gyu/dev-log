---
date: 2024-07-12
---

# TypeScript

타입스크립트는 JavaScript를 보완하는 언어로, 정적 타입을 지원한다.\
트랜스파일링을 통해 JavaScript로 변환되어야 자바스크립트 런타임 엔진에서 실행된다.

자바스크립트 런타임 엔진은 크게 아래의 종류가 있다.

- JavaScript v8 엔진 (Chrome, Node.js, Deno)
- SpiderMonkey (Firefox)
- JavaScriptCore (Safari, Bun.js)

타입스크립트를 처리하는 컴파일 엔진은 아래의 종류가 있다.

- tsc (TypeScript Compiler, Microsoft, JS 기반)
- swc (Super-fast JS/TS Compiler, swc-project, Rust 기반)
- esbuild (An extremely fast JavaScript bundler and minifier, evanw/esbuild, Go 기반)
- babel (Babel is a JavaScript compiler, babel/babel, JS 기반)

각각 프로젝트 용도와 목적에 따라 선택하여 사용한다.\
보통은 tsc를 사용해도 큰 문제가 없지만, 빌드 속도를 높이기 위해 swc나 esbuild를 사용하기도 한다.
