# TypeScript 😎

### 정의
  - 자바스크립트에 타입을 부여한 언어, 자바스크립트의 확장된 언어

### 확장자 (형식)
- .ts

### 특징
- 브라우저에서 실행하기 위해 컴파일 해주어야 함
- 빌드 시, 타입 에러와 런타임 에러는 서로 관계가 없을 수 있음

### 장점
- **API, 백엔드와의 인터페이스 약속을 정의하고 규정할 수 있음**
- 에러의 사전 방지 (Ex. 받아온 데이터의 형태를 모르는 경우, 화면에 일일이 찍어서 봐야함)
- 코드 가이드 및 자동 완성
  - 타입에 맞는 메소드 제공
  - 메소드의 자동 완성 제공

### 자바스크립트 코드에 타입스크립트를 적용할 때 주의사항
- 기능적인 변경은 절대 하지 않기
- 테스트 코드가 없을 때는 함부로 타입스크립트를 적용하지 않기
- 처음부터 타입을 엄격하게 적용하지 않기 (점진적으로 static 레벨을 증가)
  - `string`인 경우, `any`로 설정하고 컴파일을 돌렸을 때 에러가 안나는 수준만 먼저 적용 후 점진적으로 구체화

### 타입스크립트에서 ES Lint를 사용하는 이유
- `TS Lint`보다 기존의 `ES Lint`가 더 성능이 좋아서 `ES Lint` + `TS Lint`를 얹혀서 사용

### 참고 사이트
- [TypeScript Playground](https://www.typescriptlang.org/play) : ts를 js로 바로 컴파일해서 테스트 해볼 수 있는 사이트
- [Babel Try It Out!](https://babeljs.io/repl#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&corejs=3.6&spec=false&loose=false&code_lz=Q&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=env%2Creact%2Cstage-2&prettier=false&targets=&version=7.14.6&externalPlugins=) : ES6문법을 컴파일해서 테스트해볼 수 있는 사이트
