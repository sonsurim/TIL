# JS Doc
## 정의 📋
- JS 파일에 타입스크립트 language 서버를 실행하여 타입스크립트를 사용할 수 있는 환경 설정
## 장점 👍
- JS Doc + ts-check의 기능을 이용해 JS 타입을 보완
```
// @ts-check

/**
 *
 * @param {number} a 첫번째 숫자
 * @param {number} b 두번째 숫자

 */

function sum(a,b) {
  return a + b
}

sum(10, '20')
```
## 예시 📚
```
**
 * @typedef {object} Address
 * @property {string} street
 * @property {string} city
 */

/**
 * @typedef {object} User
 * @property {string} name
 * @property {string} email
 * @property {Address} address
 */

/**
 * @returns {Promise<User>}
 */
```
- - -
위의 내용은 JSDoc을 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)