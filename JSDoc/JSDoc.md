# JS Doc
## μ μ π
- JS νμΌμ νμμ€ν¬λ¦½νΈ language μλ²λ₯Ό μ€ννμ¬ νμμ€ν¬λ¦½νΈλ₯Ό μ¬μ©ν  μ μλ νκ²½ μ€μ 
## μ₯μ  π
- JS Doc + ts-checkμ κΈ°λ₯μ μ΄μ©ν΄ JS νμμ λ³΄μ
```
// @ts-check

/**
 *
 * @param {number} a μ²«λ²μ§Έ μ«μ
 * @param {number} b λλ²μ§Έ μ«μ

 */

function sum(a,b) {
  return a + b
}

sum(10, '20')
```
## μμ π
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
μμ λ΄μ©μ JSDocμ κ³΅λΆνλ©° κ°μΈμ μΌλ‘ μ λ¦¬ν λ΄μ©μλλ€.
## μΆμ² π
- [μΈνλ° κ°μ - νμμ€ν¬λ¦½νΈ μλ¬Έ κΈ°μ΄λΆν° μ€μ κΉμ§](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)