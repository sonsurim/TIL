# TypeScript ์ค์ 

## tsconfig.json ๐ 
```
{
  "compilerOptions": {
    "allowJs": true,
    "target": "ES5",
    "outDir": "./built",
    "moduleResolution": "Node",
    "lib": ["ES2015", "DOM", "DOM.Iterable"],
    "checkJs": true,
    "noImplicitAny": true,
    "typeRoots": ["./node_modules/@types", "types"],
    "strict": true,
    "strictNullChecks": true,
    "strictFunctionTypes": true,
    "strictBindCallApply": true
  },
  "include": ["./src/**/*"]
}
```

## CompilerOptions ๐ฉ

- ์ปดํ์ผํ  ๋์ ๋ถ๊ฐ์ ์ธ ์ต์๋ค
- ํ๋ก์ ํธ์ ํ์์คํฌ๋ฆฝํธ๋ฅผ ๋ณํํ  ๋ ํ์์คํฌ๋ฆฝํธ๊ฐ ์ด ํ๋ก์ ํธ๋ฅผ ์ด๋ป๊ฒ ์ดํดํ  ๊ฒ์ธ์ง์ ๋ํด ์ ์

### allowJs : Boolean
- ํ๋ก์ ํธ์์ ์๋ฐ์คํฌ๋ฆฝํธ ํ์ฉ ์ ๋ฌด
- ํ๋ก์ ํธ๋ด์ ์๋ ์๋ฐ์คํฌ๋ฆฝํธ๊น์ง ํ์์คํฌ๋ฆฝํธ๊ฐ ๊ฒ์ฆํจ

### target
- `tsc`๋ช๋ น์ด๋ก ํ์์คํฌ๋ฆฝํธ ํ์ผ์ ์๋ฐ์คํฌ๋ฆฝํธ ํ์ผ๋ก ๋ณํํด์ค ๋์ ๋์

### outDir
- ํ์์คํฌ๋ฆฝํธ์ ๊ฒฐ๊ณผ๋ฌผ์ด ์ ์ฅ๋  ์์น

### moduleResolution
```
{
  "compilerOptions": {
    "moduleResolution": "Node"
  }
}
```
- `Promise`๋ฅผ ์ธ์์์ผ์ฃผ๊ธฐ ์ํ ์ต์

### lib
- ๋ผ์ด๋ธ๋ฌ๋ฆฌ ๋ฐฐ์ด
- `"lib":["ES2015","DOM","DOM.Iterable"]` : `Promise`, `DOM` ๊ด๋ จ ์๋ฌ๊ฐ ๋จ์ง ์๊ฒ ํด์ฃผ๋ ์ค์ 

### checkJs : Boolean
- @ts-check์ฒ๋ผ ์๋ฐ์คํฌ๋ฆฝํธ์์ ํ์์คํฌ๋ฆฝํธ์ ๊ธฐ๋ฅ๋ค์ ํ์ฉํ  ์ ์์
- ํ์ ๊ฒ์ฌ ๊ธฐ๋ฅ์ ์๋ฐ์คํฌ๋ฆฝํธ์์๋ ์ฌ์ฉ ๊ฐ๋ฅ

### noImplicitAny : Boolean
- ํ์ ํ์ ๊ธฐ์
- ๋ชจ๋  ํ์์ any๋ผ๋ ๋ฃ์ด์ผํจ

## include ๐ฉ
- ํ๋ก์ ํธ ๊ธฐ์ค์ผ๋ก ํ์์คํฌ๋ฆฝํธ๋ฅผ ์ปดํ์ผํ  ์์น(๋ฒ์)
- ๊ธฐ๋ณธ๊ฐ์ `["**/*"]`
- `["./src/**/*"]` : src ํด๋ ๋ฐ์ ๋ชจ๋  ํ์ผ์ ๋์์ผ๋ก ํจ

## typeRoots ๐ฉ
- `@types` ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ์ ๊ณตํ์ง ์์ ์ง์  ์ ์ธ์ ํด์ผํ  ๋, ํด๋๋ฅผ ์ง์ ํ๋ฉด ํด๋น ํด๋์ ํ์์ ํด์ํด์ฃผ๋ ์์ฑ
```
"typeRoots": ["./node_modules/@types", "./types"]
```
- ๊ธฐ๋ณธ๊ฐ : ["./node_modules/@types"]
  - `node_modules` ํ์ `@types`๋ผ๋ ํด๋ ์์ `index.d.ts`๋ฅผ ๊ฐ์ ธ์ด

## strict ๐ฉ
- `strict: true`: `strict`์ ๊ด๋ จ๋ ์์ฑ๋ค์ด ๋ชจ๋ true๋ก ๋จ
### ์ฅ์ 
- ์ถํ์ ๋ฐ์ํ  ์ค๋ฅ ์๋ฐฉ
### strict Options
ํ์์ ์ ์ํด๋์ ์ฝ๋์์ ๋ ๊ฐ๋ ฅํ๊ฒ ํ์์ ์ ์ํ  ์ ์๊ฒ ๋์์ ์ ๊ฒํด์ฃผ๋ ์ต์

  - **strictNullChecks**
  - strictFunctionTypes
  - strictBindCallApply
  - strictPropertyInitialization
  - noImplicitThis
  - alwaysStrict

- - -
์์ ๋ด์ฉ์ TypeScript๋ฅผ ๊ณต๋ถํ๋ฉฐ ๊ฐ์ธ์ ์ผ๋ก ์ ๋ฆฌํ ๋ด์ฉ์๋๋ค.
## ์ถ์ฒ ๐
- [์ธํ๋ฐ ๊ฐ์ - ํ์์คํฌ๋ฆฝํธ ์๋ฌธ ๊ธฐ์ด๋ถํฐ ์ค์ ๊น์ง](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [์ธํ๋ฐ ๊ฐ์ - ์ค์  ํ๋ก์ ํธ๋ก ๋ฐฐ์ฐ๋ ํ์์คํฌ๋ฆฝํธ](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [์ธํ๋ฐ ๊ฐ์ - Vue.js + TypeScript ์๋ฒฝ ๊ฐ์ด๋](https://www.inflearn.com/course/vue-ts/dashboard)