# 파셜

## Partial 구현해보기 (동작 원리) 💪

Ex. `UserProfile`이라는 인터페이스를 이용하여 업데이트
```
interface UserProfile {
  username: string;
  email: string;
  profilePhotoUrl: string;
}
```
### AS-IS
```
interface UserProfileUpdate {
  username?: string;
  email?: string;
  profilePhotoUrl?: string;
}
```
- 재사용하지 않고 중복된 코드로 선언

### TO-BE
#### - 동작 원리 #1
  ```
  type UserProfileUpdate = {
    username?: UserProfile['username'];
    email?: UserProfile['email'];
    profilePhotoUrl?: UserProfile['profilePhotoUrl'];
  }
  ```
- `UserProfile`의 속성으로 접근하게 되면 타입이 나옴
#### - 동작 원리 #2
```
type UserProfileUpdate = {
   [p in 'username' | 'email' | 'profilePhotoUrl']?: UserProfile[p]
}
```
- `UserProfile`에 있는 `속성(key, 타입)`에 접근해서 선언한 type의 `속성(key, 타입)`로 설정
- 유니온 타입 안에 있는 속성들에 대해 한번씩 반복문을 실행
- 반복문이 실행될때마다 type의 `속성(key, 타입)`는 `p(유니온 타입 안의 속성)`
- 선언한 type의 `타입(value)`은 `UserProfile[key]`이 됨

#### - 동작 원리 #3
```
type UserProfileUpdate = {
  [p in keyof UserProfile]?: UserProfile[p]
}
```
- `'username' | 'email' | 'profilePhotoUrl'`은 `UserProfile`의 keyof로 대체 가능

#### - 동작 원리 #최종
```
type Subset<T> = {
  [p in keyof T]?: T[p]
}
```
- `UserProfile` 타입에 국한되지 않게 타입을 넘겨받을 수 있는 형태인 제네릭을 사용

- - -
위의 내용은 TypeScript를 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 타입스크립트 입문 기초부터 실전까지](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%85%EB%AC%B8/dashboard)
- [인프런 강의 - 실전 프로젝트로 배우는 타입스크립트](https://www.inflearn.com/course/%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8B%A4%EC%A0%84/dashboard)
- [인프런 강의 - Vue.js + TypeScript 완벽 가이드](https://www.inflearn.com/course/vue-ts/dashboard)