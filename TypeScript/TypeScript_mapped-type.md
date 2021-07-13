# 맵드 타입

## 정의 📋
- 기존에 정의되어 있는 타입을 새로운 타입으로 변환해 주는 문법
  - **AS-IS (변환 전 기존 타입)**
  ```
  {
    name: string;
    email: string;
  }
  ```
  - **TO-BE (변환 후 새 타입)**
  ```
  {
    name: number;
    email: number;
  }
  ```
## 특징 🙌
- 자바스크립트 `map()` API 함수를 타입에 적용한 것 과 같은 효과

## 문법 🔏
```
{ [ P in K ] : T }
{ [ P in K ] ? : T }
{ readonly [ P in K ] : T }
{ readonly [ P in K ] ? : T }
```

## 예시 📚
```
type Item = { a: string, b: number, c: boolean };

type T1 = { [P in "x" | "y"]: number };  // { x: number, y: number }
type T2 = { [P in "x" | "y"]: P };  // { x: "x", y: "y" }
type T3 = { [P in "a" | "b"]: Item[P] };  // { a: string, b: number }
type T4 = { [P in keyof Item]: Date };  // { a: Date, b: Date, c: Date }
type T5 = { [P in keyof Item]: Item[P] };  // { a: string, b: number, c: boolean }
type T6 = { readonly [P in keyof Item]: Item[P] };  // { readonly a: string, readonly b: number, readonly c: boolean }
type T7 = { [P in keyof Item]: Array<Item[P]> };  // { a: string[], b: number[], c: boolean[] }
```

## 예제 📚
```
type Heroes = 'Hulk' | 'Capt' | 'Thor'

type HeroAges = { [ K in Heroes ]: number }

const ages: HeroAges = {
  Hulk: 100,
  Capt: 33,
  Thor: 1000
}
```
- `Heroes` : 3개의 문자열을 유니언으로 받는 타입
- `HeroAges` : `HeroAges`를 재활용 해서 생성한 타입
  ```
  {
    Hulk: number,
    Capt: number,
    Thor: number
  }
  ```

- - -
위의 내용은 TypeScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [인프런 강의 - 실전 프로젝트로 배우는 타입스크립트](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [인프런 강의 - Vue.js + TypeScript 완벽 가이드](https://www.inflearn.com/course/vue-ts/dashboard)


