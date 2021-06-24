# TypeScript 클래스

## JavaScript Class와의 차이점
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
