# TypeScript 클래스
## JavaScript Class와의 차이점 ⚖️
### - JavaScript
```
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
```
  - `this.name, this.age` : constructor에 class에서 사용할 속성(멤버 변수)을 바로 정의 가능
  - `(name, age)` : constructor에 들어오는 파라미터에 대한 타입 지정 X

### - TypeScript
```
class Person {
  // 멤버 변수
  private name: string;
  public age: number;
  readonly log: string;

  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }
}
```
  - `this.name, this.age`
    - constructor에 class에서 사용할 속성(멤버 변수)을 바로 정의 불가능
    - class의 최상단에 멤버 변수의 타입을 정의해야 함
  - `(name, age)` : constructor에 들어오는 파라미터에 대한 타입 지정 가능
  - `private, public, readonly` : 멤버 변수에 대한 접근 범위 설정 가능

- - -
위의 내용은 TypeScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [인프런 강의 - 실전 프로젝트로 배우는 타입스크립트](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [인프런 강의 - Vue.js + TypeScript 완벽 가이드](https://www.inflearn.com/course/vue-ts/dashboard)