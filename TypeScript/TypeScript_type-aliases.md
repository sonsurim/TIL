# TypeScript 타입 별칭

## 정의 📋
- 특정 타입이나 인터페이스를 참조할 수 있는 타입 변수
- 타입을 정의할 수 있는 거의 모든 것에 별칭을 붙일 수 있음

## 특징 🙌
- 새로운 타입 생성 X
- 정의된 타입에 대해 쉽게 참고할 수 있게 이름을 부여하는 것

## 문법 🔏
- `type`이라는 키워드를 이용해서 정의
```
// 변수에 활용
type MyName = string;
const name: MyName = 'surim;

// 함수에 활용
type Todo = { id:string; title:string; done:boolean };
function getTodo(todo: Todo) {
```

## 인터페이스 vs 타입 별칭 ⚖️
### 1. 타입의 모습
- 인터페이스
<img src="./images/interface.png" width="600">

- 타입 별칭
<img src="./images/type-aliases.png" width="600">

### 2. 타입의 확장
- 인터페이스 : 확장 가능
- 타입별칭 : 확장 불가능
> 공식 문서에서는 타입 별칭보다 확장이 가능한 인터페이스를 권장하고 있다.

- - -
위의 내용은 TypeScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [인프런 강의 - 실전 프로젝트로 배우는 타입스크립트](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [인프런 강의 - Vue.js + TypeScript 완벽 가이드](https://www.inflearn.com/course/vue-ts/dashboard)