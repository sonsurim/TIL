# TypeScript 연산자

## 유니온 타입
### 정의
- 특정 파라미터나 변수에 한가지 이상의 타입을 사용하고 싶을 때 파이프 연산자를 통해 사용

### 특징
- **인터페이스나 특정 구조체를 유니온 타입으로 쓰는 경우, 공통 속성만 제공**

![interface](/TypeScript/images/operator_interface.png)
  someone에 어떤 값이 들어올 지 모르기 때문에 Developer의 skill이나 Person의 age가 아닌 보장된 속성만 제공

### 장점
- 특정 타입을 자동으로 추론해서 해당 타입에 맞는 메소드 제공
![any](/TypeScript/images/operator_any.png)
![연산자](/TypeScript/images/operator.png)
### 문법
```
let surim: string | number;

function logMessage(value: string | number) {
  if (typeof value === 'number') {
    value.toLocaleString();
  }

  if (typeof value === 'string') {
    value.toString();
  }

  throw new TypeError('value must be string or number!');
}
```
