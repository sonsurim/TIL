# TypeScript 타입 추론

## 정의
- 코드를 작성했을 때 해당 코드의 타입이 무엇인가에 대해 정의하는 방식이자 동작

## 특징
- 기본적인 변수의 선언과 할당에 의해서 타입이 추론됨

## 동작 과정
변수 선언, 속성, 인자의 기본 값, 함수의 반환 값 등을 설정할 때 타입추론이 발생
```
let x = 3;
```
1. TS 파일이기 때문에 VS Code 내부적으로 lauguage 서버가 동작
2. Lauguage 서버가 동작하면서 타입을 추론 시작

```
let a = 'abc';

// b: any
function getB (b) {
  return b;
}

// b: string (숫자 + 문자열 = 문자열)
function getB(b = 10) {
  let c = 'hi';
  return b + c;
  return b;
}
