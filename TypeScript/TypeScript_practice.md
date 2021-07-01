# TypeScript 실무

## 타입스크립트 기본 환경 구성
### 1. NPM 초기화
```
npm init
```

### 2. 타입스크립트 라이브러리 설치
```
npm i -g typescript
```
### 3. [타입스크립트 설정 파일 생성 및 기본 값 추가](https://www.typescriptlang.org/tsconfig)
```
{
  "compilerOptions": {
    "allowJs": true,
    "checkJs": true,
    "noImplicitAny": true
  }
}
```

## 자바스크립트 환경을 타입스크립트로 변환하기
### 1. JSDoc
```
// @ts-check
```
- JS 파일에 타입스크립트 language 서버를 실행하여 타입스크립트를 사용할 수 있는 환경 설정