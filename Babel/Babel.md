# 바벨
## 정의 📋
- 자바스크립트 컴파일러
- 최신 자바스크립트 문법이 최대한 많은 브라우저에서 호환될 수 있게 변경해주는 도구
> 컴파일? 브라우저에서 실행할 수 있는 용도로 변환해주는 것

## 동작 💪
- **AS-IS**
  ```
  const sum = (a, b) => {
    return a + b;
  }
  ```
- **TO-BE**
  ```
  var sum = function sum(a, b) {
    return a + b;
  }
  ```

## 타입스크립트에서 바벨 사용 🛠
```
npm i -D @babel/preset-typescript
```
> @babel : babel이 제공해주는 organization을 의미

### preset
- 바벨에서의 preset? 플러그인 + 옵션들을 포함, 특정값들의 집합

### preset 사용 이유
- babel이 타입 시스템을 이해할 수 없기 때문에 `@babel-preset`을 사용해야 함

- - -
위의 내용은 Babel을 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
