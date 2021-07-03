# TypeScript 실무 - 자바스크립트 환경을 타입스크립트로 변환하기

## 타입스크립트 기본 환경 구성
### 1. NPM 초기화
```
npm init
```

### 2. 타입스크립트 라이브러리 설치
```
npm i typescript --save -dev
```
### 3. [타입스크립트 설정 파일(tsconfig.json) 생성 및 기본 값 추가](https://www.typescriptlang.org/tsconfig)
```
{
  "compilerOptions": {
    "allowJs": true,
    "target": "ES5",
    "outDir": "./built",
    "moduleResolution": "Node",
  },
  "include": ["./src/**/*"]
}
```

### 4. 자바스크립트 파일을 타입스크립트 파일로 변환
- **app.js** → **app.ts**

### 5. `tsc` 명령어로 타입스크립트 컴파일
```
tsc
```

## 타입스크립트 에러 디버깅 방법
![](/TypeScript/images/ts_error.png)
1. **(ts2705)** 에러코드 구글링
2. 에러메시지 마지막 문장 복사해서 구글링

![](/TypeScript/images/ts_solution.png)