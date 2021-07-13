# TypeScript function

## parameters / return 🛠
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

## 옵셔널 파라미터 🔩
- 특정 파라미터를 선택적으로 사용하고 싶은 경우
```
function log(a: string, b: string, c?:string) {}

log('a', 'b') // c를 쓰지 않아도 오류 X
```

- - -
위의 내용은 TypeScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [인프런 강의 - 실전 프로젝트로 배우는 타입스크립트](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [인프런 강의 - Vue.js + TypeScript 완벽 가이드](https://www.inflearn.com/course/vue-ts/dashboard)