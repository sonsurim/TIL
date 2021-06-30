# TypeScript 타입 호환

## 정의
- 타입스크립트 코드에서 특정 타입이 다른 타입에 잘 맞는지를 의미
- 타입스크립트가 코드를 해석해나가는 과정에서 두개의 타입이 서로 호환이 되는지 점검하는 것

## 특징
- 할당되는 타입(왼쪽)이 더 많은 속성을 가지거나 구조적으로 더 컸을 때만 할당하려는 타입(오른쪽)과 호환이 됨
- 타입 스크립트에서 코드간에 타입이 서로 맞는지 확인할 떼는, **내부적으로 존재하고 있는 속성과 타입에 대한 정의들에 대해서 비교를 함**

## 예제

### 1. 인터페이스
```
interface Developer {
  name: string;
  skill: string;
}

interface Person {
  name: string;
}

let developer: Developer;
var person: Person;
developer = person; // Error
```

### 2. 함수
```
let add = function(a: number) {
  // ...
}

let sum = function(a:number, b:number) {
  // ...
}

add = sum // Error
sum = add
```
- `add = sum` : sum은 두 개의 인자를 넘겨줘야 하는데 adds는 하나의 인자만 받을 수 있음 > 호환 불가
- `sum = add`: add는 파라미터를 하나 가지는 함수, sum은 파라미터를 2개 가지는 함수 > 호환 가능

### 3. 제네릭
```
//Case1. Empty
interface Empty<T> {
// ...
}

let empty1: Empty<string>;
let empty2: Empty<number>;
empty1 = empty2;
empty2 = empty1;

// Case2. NotEmpty
interface NotEmpty<T> {
  data: T;
}

let notempty1: NotEmpty<string>;
let notempty2: NotEmpty<number>;
notempty1 = notempty2; //Error
notempty2 = notempty1; //Error
```
- `interface Empty`
  - 내부 구조적으로 비어있기 때문에 어떤값이 들어와도 서로 동일한 타입이라고 간주를 하게 됨
  - 서로 호환 가능
- `interface NotEmpty`
  - 동일한 속성은 있지만 오른쪽의 타입(`T`)이 달라짐 > 구조적인 타입의 차이가 생김
  - 서로 호환 불가