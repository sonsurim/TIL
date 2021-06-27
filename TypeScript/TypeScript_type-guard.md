# TypeScript 타입 가드

## 정의
- 타입의 범위를 점점 줄여가며 구체화해 나가는 것

## 사용 예시
### AS-IS
```
interface Developer {
  name: string;
  skill: string;
}

interface Person {
  name: string;
  age: number;
}

function introduce(): Developer | Person {
  return { name: 'Surim', age: 33, skill: 'Iron Making' }
}

let surim = introduce();
console.log(surim.skill); // Error: skill에 접근 불가
```
- 의도적으로 객체를 리턴하고 있지만 유니온 타입은 **타입들의 공통된 속성만 접근 가능**

### TO-BE - 타입 단언
```
if ( (surim as Developer).skill ) {
  let skill = (surim as Developer).skill;
  console.log(skill);

} else if ( (surim as Person).age ) {
  let age = (surim as Person).age
  console.log(age);
}
```
- 위와 같이 타입 단언을 사용해서 타입의 구체화를 시킬 수 있음
- 내부 코드에 접근하기 위해 계속해서 코드 단언을 해주어야 하는 문제

### TO-BE - 타입 가드
```
function isDeveloper(target: Developer | Person): target is Developer {
  return (target as Developer).skill !== undefined;
}

if (isDeveloper(surim)) {
  console.log(surim.skill); // target: Developer
} else {
  console.log(surim.age);   // target: Person
}
```
- `target`이 `Developer` 타입이라고 가정하고 `skill`이라는 값이 있는 경우, `target`이 `Developser` 타입이라고 취급