# Async & Await
## 정의
- 자바스크립트 비동기 처리 패턴의 최신 문법

## 특징
- `Promise`와 `Generate`조합으로 구성되어 있음
- Promise와 Callback에서 주는 단점들을 해결
- 비동기 함수를 동기적으로 코드를 작성할 수 있게 도와줌

## 문법
```
async function fetchData() {
  await getUserList();
}
```
- 비동기로 처리할 함수에 `async`라는 키워드를 붙임
- 비동기로 처리할 함수 내부의 비동기 처리 코드에 `await`라는 키워드를 붙임
> 비동기로 처리할 함수 == Promise 객체를 반환하는 API 호출

## 자바스크립트의 비동기 처리
- 자바스크립트는 동기적으로 실행되는 것이 기본 (== 동기적 사고에 익숙 )

  → 비동기 처리 함수는 비동기적 사고로 대응해야 함

### AS-IS #1. callback

```
function fetchData() {
  $.ajax('users/1', function(user) {
    console.log(user);
    $.ajax('user/2', ...)
  });
  console.log(user);
}

let a = 10;
console.log(a);
let sum = a * 2;
console.log(sum);
```
- 콜백 내부에 콜백을 선언하여 콜백지옥 생성

### AS-IS #2. Promise
```
$.ajax.then().then().then() ...
```
- `then`으로 불필요한 맵핑
### TO-BE #1. Async&Await
```
async function fetchData() {
  const user = await $.ajax('users/1');
}
```
- 내부적으로는 비동기 처리지만 외부에서 보았을 때 비동기 처리할 필요 없이 **동기적 사고로 처리 가능**
