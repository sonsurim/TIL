# 자바스크립트 함수

## ES5 - 함수 선언문 📚
- `function`이라는 키워드를 이용해서 함수를 생성
```
function sum(a, b) {
  return a + b;
}
```
## ES5 - 함수 표현식 📚
- 함수를 생성 후 변수에 함수의 참조값을 넣음
```
var sum = function(a, b) {
  return a + b;
}
```
## ES6+ - 함수 표현식(화살표 함수) 📚
- `function`이라는 글자를 화살표로 대체
- 코드 라인수를 줄이고 가독성을 향상시켜 등장한 문법
```
let sum = (a,b) => {
  return a + b;
}

let sum = (a,b) => a + b;
```
### 타입스크립트의 화살표 함수
```
let sum = (a: number, b: number): number => {
  return a + b
}
```

- - -
위의 내용은 JavaScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)