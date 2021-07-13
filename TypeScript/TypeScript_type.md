# TypeScript 타입

## 기본 타입 🛠
- Boolean
  ```
  let show: boolean = true;
  ```
- Number
  ```
  let num: number = 10;
  ```
- String
  ```
  var str: String = 'hello';
  ```
- Object
  ```
  // 선언 타입 1.
  let obj: object = {};

  // 선언 타입 2. 특정 속성과 속성의 값까지 타입 정의
  let person: { name: string, age: number } = {
    name: 'surim',
    age: 24
  };
  ```
- Array
  ```
  // 선언 타입 1.
  let arr: Array<number> = [1,2,3];

  // 선언 타입 2.
  let arr: number[] = [1,2,3];
  ```
- Tuple
  - 모든 인덱스에 타입이 정의되어 있는 배열
  ```
  let address: [string, number] = ['gangnam', 100];
  ```
- [Enum](https://github.com/sonsurim/TIL/commit/9146bfbfa8b2b24b7f65811405eb428b08085096)
  - 특정 값들의 집합을 의미하는 자료형

- Any
  - string,number,array 등의 모든 타입
  - 실행하는 시점에 타입을 자동으로 할당
  ```
  let items: Any;

  let items: Any = [];
  ```
- Void
    - 반환값이 없다고 명시적으로 지정
  ```
  function addTodo(todo: object[]): void {
    todoItems.push(todo);
  };
  ```

- Element
  - `Element`: element 중 가장 상위에 있는 타입 구조체
  - `HTMLElement`: `Element` 하위에 상속을 받아 확장한 타입
  - `HTMLParagraphElement`: `HTMLElement`를 더 구체화 시킨 타입 (`p`태그)
  - `HTMLSpanElement`: `HTMLElement`를 태그별로 더 구체화시킨 타입 (`span`태그)
  ```
  let a: Element | HTMLElement | HTMLParagraphElement
  ```

- Null
- Undefined
- Never

- - -
위의 내용은 TypeScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [인프런 강의 - 실전 프로젝트로 배우는 타입스크립트](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [인프런 강의 - Vue.js + TypeScript 완벽 가이드](https://www.inflearn.com/course/vue-ts/dashboard)