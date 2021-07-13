# JavaScript 구조 분해 문법
## 자바스크립트에서의 구조 🔩
- `왼쪽: 변수 이름 = 오른쪽: 데이터 타입`과 같은 선언 형식
```
const arr = [1, 2, 3, 4];

const obj = {
  a: 10,
  b: 20,
  c: 30
};
```
## 자바스크립트에서의 구조 분해 ⚙️
- 변수 선언 형식이 자유로워지는 것
```
// AS-IS
const a = obj.a;
const b = obj.b;
const c = obj.c;

// TO-BE
const { a, b, c } = obj;
console.log(a) //10
```

## 문법 - 별칭 🔏
```
const { 가져올 변수명: 새롭게 지을 변수명 } = 가져올 곳;
```
### 사용 예시
```
const { a: newA } = obj;
console.log(newA) // 10, obj.a와 동일
```

- - -
위의 내용은 JavaScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)