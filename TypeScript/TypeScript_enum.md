# TypeScript μ΄λ

## μ μ π
- νΉμ  κ°λ€μ μ§ν©μ μλ―Ένλ μλ£ν
- νμμ€ν¬λ¦½νΈμμ μ«μν μ΄λ, λ¬Έμν μ΄λ μ κ³΅

## νΉμ§ π
- enumμ μ¬μ©νμ λ λ³λμ κ°μ μ¬μ©νμ§ μμΌλ©΄ κΈ°λ³Έκ°μΌλ‘ `μ«μ 0`μ ν λΉν¨
## μ«μν μ΄λ π©
```
enum Shoes {
  Nike,       // 0
  Adidas,     // 1
  NewBalance  // 2
}

let myShoes = Shoes.Nike;
console.log(myShoes); // 0
```
<img src="./images/enum.png" width="600" />

- κ°μ μ΄μ©νμ§ μλ κ²½μ°, μλμΌλ‘ μ«μλ₯Ό ν λΉ

```
enum Shoes {
  Nike = 10,   // 10
  Adidas,      // 11
  NewBalance   // 12
}

let myShoes = Shoes.Nike;
console.log(myShoes); // 10
```
- λ€λ₯Έ μ«μλ₯Ό μ΄κΈ°νλ₯Ό νλ κ²½μ° μλμΌλ‘ 1μ© μ¦κ°ν΄μ ν λΉ

## λ¬Έμν μ΄λ π©
<img src="./images/enum_text.png" width="600" />

```
enum Shoes {
  Nike = 'λμ΄ν€',
  Adidas = 'μλλ€μ€'
}

let myShoes = Shoes.Nike;
console.log(myShoes); // 'λμ΄ν€'
```

## νμ© μμ π
- **AS-IS (string)**
    ```
    function askQuestion(answer: string) {
      if (answer === 'yes') {
      console.log('μ λ΅μλλ€!');
      }
      if (answer === 'no') {
        console.log('μ€λ΅μλλ€!');
      }
    }

    askQuestion('μμ€');
    askQuestion('Y');
    askQuestion('yes');
    ```
    λ€μν ννμ λ¬Έμμ΄μ λ£μ μ μμ

- **To-BE (Enum)**
    ```
    enum Answer {
      Yes = 'Y',
      No = 'N'
    }

    function askQuestion(answer: Answer) {
      if (answer === Answer.Yes) {
      console.log('μ λ΅μλλ€!');
      }
      if (answer === Answer.No) {
        console.log('μ€λ΅μλλ€!');
      }
    }

    askQuestion(Answer.Yes);
    askQuestion('Yes');       // Error!
    askQuestion('μμ€');       // Error!
    askQuestion('Y');         // Error!
    ```
    - λ¬Έμμ΄μ κ΅¬μ²΄μ μΈ κ°μΌλ‘ μ§μ 
    - μ΄λμ μ΄μ©ν μ μκΈ° λλ¬Έμ 'Yes'λ μ€λ₯ λ°μ
    - μ΄λμμ μ κ³΅νλ λ°μ΄ν°λ§ λκΈΈ μ μμ

- - -
μμ λ΄μ©μ TypeScriptλ₯Ό κ³΅λΆνλ©° κ°μΈμ μΌλ‘ μ λ¦¬ν λ΄μ©μλλ€.
## μΆμ² π
- [μΈνλ° κ°μ - νμμ€ν¬λ¦½νΈ μλ¬Έ κΈ°μ΄λΆν° μ€μ κΉμ§](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [μΈνλ° κ°μ - μ€μ  νλ‘μ νΈλ‘ λ°°μ°λ νμμ€ν¬λ¦½νΈ](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [μΈνλ° κ°μ - Vue.js + TypeScript μλ²½ κ°μ΄λ](https://www.inflearn.com/course/vue-ts/dashboard)
