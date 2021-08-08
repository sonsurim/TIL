# [Altong 스터디 2주차 (2021.08.06)]()

## 기간 📆

- 2021.07.23 ~ 2021.08.06 (여러 이슈들로 재정비 기간을 거침)

## 내용 📚

- 새로운 팀원 소개
- github 운영 방식 논의
- 스터디 운영 방식 논의
- 문제 발표

## 결과물 💪

- [알통스터디 2주차 발표 과제](https://www.notion.so/herman94/Section-1-No-10-88ae374a8bcc4f00bed2ae884c77befd)
- [알통스터디 2주차 피드백 노트](https://www.notion.so/herman94/2-f3812794045849399126923db44852c2)

## 배운 점 / 느낀 점 🤩

- `reduce`메서드에 대해 깊이 알게 되었다.

  ```
  acc = prev
  cur = next
  ```

  - `reduce`에서 리턴값이 그 다음 동작할 때 `prev`에 할당되기 때문에 어떤 값이 `return`되는지가 중요!

- `iterator`에 대해 알게되었지만 조금 더 학습이 필요할 것 같다!

  ```
  const str = new String('od');
  str[Symbol.iterator]().next();

  const itr = str[Symbol.iterator]().next();
  itr.next();
  itr.next();
  ```

  - 처음에 문자열을 가리킴
  - `done`: iterator가 동작을 여부 결정
  - `done: true` : 동작 중지

- `for...of`문의 동작 원리에 대해 다시 한번 생각해보게 되었다!

  ```
  for(let char of string) {
    console.log(char);
  }
  ```

  - `for...of`는 내부적으로 `iterator.next()` 함수가 호출되면서 값이 더 있는 경우, 값을 더 들고오는 형태로 동작한다.

    - `for...of`에서 `iterator`의 `next()`가 호출
    - `for`문과 `iterator`가 반복 실행

    - 문자열은 `Symbol.iterator`를 내장하고 있다!

      → `for ...of`문 사용 가능

    - 객체는 `Symbol.iterator`를 내장하고 있지 않다!

      → `for ...of`문 사용 가능

- `label`을 이용한 코드를 처음 보았다! 뭔가 이론상으로는 얼핏 들었던 기억이 있는데 실제로 보니 신기했다! 얼른 `label`에 대해서 학습을 해보아야겠다.
- `substr`이 MDN한국 페이지에서 사용중지 알림을 띄웠다는 사실을 알게 되었다! 이는 단점이 있고 문제점이 있어서 그렇다는데 앞으로 `substr` 사용을 지양하고 `substring` 사용을 지향해야겠다.

---

## 과제 📝

- [인프런 - 자바스크립트 알고리즘 문제 풀이 미정](https://www.inflearn.com/course/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4/dashboard)

### 발표 문제

- 미정
