# JS Doc

## Javscript에서의 타입 정의
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

### JS Doc 예시
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