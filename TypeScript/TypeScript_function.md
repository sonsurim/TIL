# TypeScript function

## parameters / return ๐ 
  ```
  // 1. ํจ์์ ํ๋ผ๋ฏธํฐ์ ํ์์ ์ ์ํ๋ ๋ฐฉ์
  function sum(a: number, b: number) {
    return a + b;
  };

  sum(10,20);


  // 2. ํจ์์ ๋ฐํ ๊ฐ์ ํ์์ ์ ์ํ๋ ๋ฐฉ์
  function sum(): number {
    return 10;
  }


  // 3. ๊ธฐ๋ณธ์ ์ธ ๋ฐฉ์ ( 1 + 2 )
  function sum(a: number, b: number): number {
    return a + b;
  }
  ```

## ์ต์๋ ํ๋ผ๋ฏธํฐ ๐ฉ
- ํน์  ํ๋ผ๋ฏธํฐ๋ฅผ ์ ํ์ ์ผ๋ก ์ฌ์ฉํ๊ณ  ์ถ์ ๊ฒฝ์ฐ
```
function log(a: string, b: string, c?:string) {}

log('a', 'b') // c๋ฅผ ์ฐ์ง ์์๋ ์ค๋ฅ X
```

- - -
์์ ๋ด์ฉ์ TypeScript๋ฅผ ๊ณต๋ถํ๋ฉฐ ๊ฐ์ธ์ ์ผ๋ก ์ ๋ฆฌํ ๋ด์ฉ์๋๋ค.
## ์ถ์ฒ ๐
- [์ธํ๋ฐ ๊ฐ์ - ํ์์คํฌ๋ฆฝํธ ์๋ฌธ ๊ธฐ์ด๋ถํฐ ์ค์ ๊น์ง](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [์ธํ๋ฐ ๊ฐ์ - ์ค์  ํ๋ก์ ํธ๋ก ๋ฐฐ์ฐ๋ ํ์์คํฌ๋ฆฝํธ](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [์ธํ๋ฐ ๊ฐ์ - Vue.js + TypeScript ์๋ฒฝ ๊ฐ์ด๋](https://www.inflearn.com/course/vue-ts/dashboard)