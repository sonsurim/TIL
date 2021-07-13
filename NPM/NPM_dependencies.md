# NPM dependencies
## 배포용 라이브러리 (dependencies) 🛠
- 화면의 애플리케이션의 로직과 직접적인 연관이 있는 라이브러리
- 애플리케이션을 동작시킬때 필요한 라이브러리
- 화면단 라이브러리

### 명령어
```
npm i <패키지명>

npm i jquery
```
### 예시
```
//package.json

{
  ...
  "dependencies": {
    "jquery": "",
    "jquery-ui": "",
    "react": "",
    "angular": "",
    "vue": "",
    "chart": ""
  }
}
```
- **jquery**: 화면의 DOM을 조작하기 위한 유틸성 라이브러리
- **jquery-ui**: jquery의 화면 DOM조작을 도와주는 부가적인 라이브러리

## 개발용 라이브러리 (devDependencies) 🛠
- 개발을 할 때 도움을 주는 개발 보조 라이브러리

### 명령어
```
npm i <패키지명> -D

npm i jquery -D
```
### 예시
```
//package.json

{
  ...
  "dependencies": {
    "webpack": "",
    "js-compression": "",
    "sass": ""
  }
}
```
- **js-compression**: javascript 압축 도구
- **sass**: css 전처리기

## 주의사항 🔏
- 개발용 라이브러리들은 빌드를 하고 최종 서버에 배포를 할 때 배포가 되지 않음

  (package.json의 devDependencies에 있는 라이브러리)

- 구분해서 넣지 않는 경우, 빌드 시간에도 영향이 미칠 수 있음
- - -
위 내용은 NPM을 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 프론트엔드 개발자를 위한 웹팩](https://www.inflearn.com/course/%ED%94%84%EB%9F%B0%ED%8A%B8%EC%97%94%EB%93%9C-%EC%9B%B9%ED%8C%A9)