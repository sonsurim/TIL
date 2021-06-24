# TypeScript 타입

## 기본
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

- Null
- Undefined
- Never
