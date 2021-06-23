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
- Enum
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

## 함수
- parameters / return
  ```
  // 1. 함수의 파라미터에 타입을 정의하는 방식
  function sum(a: number, b: number) {
    return a + b;
  };

  sum(10,20);


  // 2. 함수의 반환 값에 타입을 정의하는 방식
  function sum(): number {
    return 10;
  }


  // 3. 기본적인 방식 ( 1 + 2 )
  function sum(a: number, b: number): number {
    return a + b;
  }
  ```

- 옵셔널 파라미터
  - 특정 파라미터를 선택적으로 사용하고 싶은 경우
  ```
  function log(a: string, b: string, c?:string) {
  }

  log('a', 'b') // c를 쓰지 않아도 오류 X
  ```