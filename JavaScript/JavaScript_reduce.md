# Array.prototype.reduce()
## 정의 📋
- 배열의 각각의 아이템들을 순회하면서 이전 연산값에 대해 누적시키며 최종적으로 하나의 값을 반환하는 내장 API
## 문법 🔏
**`reduce` 콜백 함수에 꼭 리턴을 해주어야 값이 누적됨**
```
const array1 = [1, 2, 3, 4];
const reducer = ( accumulator, currentvalue ) => accumulator + currentValue;

// 1 + 2 + 3 + 4
console.log(array1.reduce(reducer));
// 10
```
- `array1`에 reduce를 실행시켜 배열 각각의 요소들을 더한 뒤 , 최종 값을 반환
- `accumulator`: 요소들의 누적치 계산된 누적치, 최종적으로 `accumulator`에 쌓여있는 값들이 반환
- `currentValue`: 각각의 요소들 접근할 때 마다 해당 요소
- **parameter**
  - 첫번째 파라미터 : 어떤식으로의 연산을 실행할 건지에 대한 콜백
  - 두번째 파라미터: initial value, 초기값 설정 가능

## 예시 📚
```
const heroes = [
  {name: 'capt', age: 100},
  {name: 'thor', age: 1000}
]

heroes.reduce((total, currentItem) => {
  total = total + total.currentItem.age;
  return total;
}, 0)
```
`0`: `initial value`, 초기값

- - -
위의 내용은 JavaScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)