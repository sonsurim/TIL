# TypeScript 설정

## tsconfig.json
```
{
  "compilerOptions": {
    "allowJs": true,
    "checkJs": true,
    "noImplicitAny": true
  }
}
```

### compilerOptions : Object
- 컴파일할 때의 부가적인 옵션들
- 프로젝트의 타입스크립트를 변환할 때 타입스크립트가 이 프로젝트를 어떻게 이해할 것인지에 대해 정의

### allowJs : Boolean
- 프로젝트에서 자바스크립트 허용 유무

### checkJs : Boolean
- @ts-check처럼 자바스크립트에서 타입스크립트의 기능들을 활용할 수 있음
- 타입 검사 기능을 자바스크립트에서도 사용 가능

### noImplicitAny : Boolean
- 타입 필수 기입
- 모든 타입을 any라도 넣어야함