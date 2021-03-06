# TypeScript 설정

## tsconfig.json 🛠
```
{
  "compilerOptions": {
    "allowJs": true,
    "target": "ES5",
    "outDir": "./built",
    "moduleResolution": "Node",
    "lib": ["ES2015", "DOM", "DOM.Iterable"],
    "checkJs": true,
    "noImplicitAny": true,
    "typeRoots": ["./node_modules/@types", "types"],
    "strict": true,
    "strictNullChecks": true,
    "strictFunctionTypes": true,
    "strictBindCallApply": true
  },
  "include": ["./src/**/*"]
}
```

## CompilerOptions 🔩

- 컴파일할 때의 부가적인 옵션들
- 프로젝트의 타입스크립트를 변환할 때 타입스크립트가 이 프로젝트를 어떻게 이해할 것인지에 대해 정의

### allowJs : Boolean
- 프로젝트에서 자바스크립트 허용 유무
- 프로젝트내에 있는 자바스크립트까지 타입스크립트가 검증함

### target
- `tsc`명령어로 타입스크립트 파일을 자바스크립트 파일로 변환해줄 때의 대상

### outDir
- 타입스크립트의 결과물이 저장될 위치

### moduleResolution
```
{
  "compilerOptions": {
    "moduleResolution": "Node"
  }
}
```
- `Promise`를 인식시켜주기 위한 옵션

### lib
- 라이브러리 배열
- `"lib":["ES2015","DOM","DOM.Iterable"]` : `Promise`, `DOM` 관련 에러가 뜨지 않게 해주는 설정

### checkJs : Boolean
- @ts-check처럼 자바스크립트에서 타입스크립트의 기능들을 활용할 수 있음
- 타입 검사 기능을 자바스크립트에서도 사용 가능

### noImplicitAny : Boolean
- 타입 필수 기입
- 모든 타입을 any라도 넣어야함

## include 🔩
- 프로젝트 기준으로 타입스크립트를 컴파일할 위치(범위)
- 기본값은 `["**/*"]`
- `["./src/**/*"]` : src 폴더 밑의 모든 파일을 대상으로 함

## typeRoots 🔩
- `@types` 라이브러리를 제공하지 않아 직접 선언을 해야할 때, 폴더를 지정하면 해당 폴더의 타입을 해석해주는 속성
```
"typeRoots": ["./node_modules/@types", "./types"]
```
- 기본값 : ["./node_modules/@types"]
  - `node_modules` 하위 `@types`라는 폴더 안의 `index.d.ts`를 가져옴

## strict 🔩
- `strict: true`: `strict`와 관련된 속성들이 모두 true로 됨
### 장점
- 추후에 발생할 오류 예방
### strict Options
타입을 정의해놓은 코드에서 더 강력하게 타입을 정의할 수 있게 동작을 점검해주는 옵션

  - **strictNullChecks**
  - strictFunctionTypes
  - strictBindCallApply
  - strictPropertyInitialization
  - noImplicitThis
  - alwaysStrict

- - -
위의 내용은 TypeScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [인프런 강의 - 실전 프로젝트로 배우는 타입스크립트](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [인프런 강의 - Vue.js + TypeScript 완벽 가이드](https://www.inflearn.com/course/vue-ts/dashboard)