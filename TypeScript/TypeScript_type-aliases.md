# TypeScript 타입 별칭

## 정의
- 특정 타입이나 인터페이스를 참조할 수 있는 타입 변수
- 타입을 정의할 수 있는 거의 모든 것에 별칭을 붙일 수 있음

## 특징
- 새로운 타입 생성 X
- 정의된 타입에 대해 쉽게 참고할 수 있게 이름을 부여하는 것

## 문법
- `type`이라는 키워드를 이용해서 정의
```
// 변수에 활용
type MyName = string;
const name: MyName = 'surim;

// 함수에 활용
type Todo = { id:string; title:string; done:boolean };
function getTodo(todo: Todo) {
```

## 인터페이스 vs 타입 별칭
### 1. 타입의 모습
- 인터페이스
![인터페이스](/TypeScript/images/interface.png)
- 타입 별칭
![타입별칭](/TypeScript/images/type-aliases.png)

### 2. 타입의 확장
- 인터페이스 : 확장 가능
- 타입별칭 : 확장 불가능
> 공식 문서에서는 타입 별칭보다 확장이 가능한 인터페이스를 권장하고 있다.