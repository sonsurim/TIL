# TypeScript 설정

## tsconfig.json
```
{
  "compilerOptions": {
    "allowJs": true,
    "target": "ES5",
    "outDir": "./built",
    "moduleResolution": "Node",
    "lib": ["ES2015", "DOM", "DOM.Iterable"],
    "checkJs": true,
    "noImplicitAny": true
  },
  "include": ["./src/**/*"]
}
```

## CompilerOptions

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

## include
- 프로젝트 기준으로 타입스크립트를 컴파일할 위치(범위)
- 기본값은 `["**/*"]`
- `["./src/**/*"]` : src 폴더 밑의 모든 파일을 대상으로 함