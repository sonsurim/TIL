# TypeScript function

## parameters / return
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

## 옵셔널 파라미터
- 특정 파라미터를 선택적으로 사용하고 싶은 경우
```
function log(a: string, b: string, c?:string) {}

log('a', 'b') // c를 쓰지 않아도 오류 X
```