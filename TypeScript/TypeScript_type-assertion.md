# TypeScript 타입 단언

## 정의
- **타입스크립트한테 개발자가 정의한 타입으로 정의를 하는 것**

## 특징
- DOM API를 조작할 때 주로 사용됨

## 문법
### AS-IS
```
let a;        // a: any

a = 20;       // a: number
a = 'a';      // a: string

let b = a;    // b: any
```
- 타입 추론 방식으로 할당 이전의 코드들을 추적할 수 없고 추론할 수 없어서 초기 타입인 `any`를 `b`에 할당

### TO-BE
```
let a;        // a: any

a = 20;       // a: number
a = 'a';      // a: string

let b = a as string;    // b: string
```
- 타입을 `string`으로 지정해줌

## 사용 예제
### DOM API 조작
> DOM API ? document라는 속성에서 제공하는 속성 또는 API이자, 웹 페이지의 태그 정보를 접근하고 조작할 수 있는 API

#### AS-IS
```
let div = document.querySelector('div');  // div: HTMLDivElement | null

if ( div ) {
  div.innerText
}
```
- div가 있는지 체크 후에 해당하는 DOM API 사용 가능
#### TO-BE
```
let div = document.querySelector('div') as HTMLDivElement  // div: HTMLDivElement

div.innerText;
```
- 타입 단언을 통해 따로 확인 절차 거칠 필요 없이 바로 DOM API 사용 가능