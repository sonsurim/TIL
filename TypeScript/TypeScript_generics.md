# TypeScript 제네릭

## 정의
- 호출하는 시점에 문자열, 숫자 등 타입을 넘겨줄 수 있는 것
## 특징
- 타입을 마치 함수의 파라미터의 개념으로 받음
  - 함수를 호출할 때 파라미터에 대한 타입을 지정해서 보낼 수 있음
- C#, Java 등 타입이 들어간 언어에서 가장 많이 활용됨
- 재사용성이 높은 컴포넌트를 만들 때 자주 활용됨

## 장점
- 정확한 타입 추론으로 해당하는 메소드 사용 가능

## 문법
```
function logText<T>(text: T): T {
  console.log(text);
  return text;
}

logText<string>('안녕')
```
- `<string>` : logText 함수 내부에서 처리하는 text에 대한 타입은 파라미터로 받은 string
- `logText<string>('안녕')`
  - logText라는 함수에 인자를 넘김
  - 해당 인자의 타입은 string이라고 generic으로 직접 정의

## 기존 타입 vs 유니온 타입 vs 제네릭
### - 기존 타입
```
function logText(text: string) {
  console.log(text);
  return text;
}

function logNumber(num: number) {
  console.log(num);
  return num;
}

logText('a');
const num = logNumber(10);
```
- 타입을 다르게 받기 위해 중복되는 코드들을 생산하게 됨

### - 유니온 타입
```
function logText(text: string | number) {
  console.log(text);
  text.
  return text;
}

const a = logText('a');
console.log(a);
logText(10);
```
- 타입을 다르게 보낼때의 문제는 해결됨 (input에 대한 문제)
- 공통으로 접근할 수 있는 속성이나 API에 대해서만 자동완성 제공 (output에 대한 문제)
- 반환 타입이 정확하게 추론되지 않음 > 해당 타입에 대한 메소드 사용 불가 (output에 대한 문제)
### - 제네릭
```
function logText<T>(text: T): T {
  console.log(text);
  return text;
}

const abc = logText<string>('abc');

abc.toString()

const login = logText<boolean>(true);
```
- `<T>` : 제네릭 사용 선언
  - 함수를 정의할 때 받은 타입을 파라미터의 타입으로 정의
  - 리턴값의 타입으로 정의
- 호출할 때 타입 정의 > 인자와 반환값 타입 자동 정의
- 정확한 타입 추론 > 해당하는 메소드 사용 가능
