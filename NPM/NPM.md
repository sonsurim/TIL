# NPM (Node Package Manager)

## 정의 📋
- 자바스크립트 프로그래밍 언어를 위한 패키지(라이브러리) 관리자
- 자바스크립트 라이브러리를 관리해주는 도구
- 전 세계의 모든 자바스크립트 라이브러리들이 있는 공개 저장소

  (Ex. jQuery, tensorflow 등)

## 특징 👋
> NPM은 Node.js를 설치하면 같이 설치됨

- 간단한 프론트엔드 프레임워크 뿐만 아니라 node.js 관련된 express 라이브러리, 머신러닝, IOT 등 전체적인 자바스크립트 라이브러리를 검색해서 받고 확인가능
- 자바스크립트로 무언가를 만들고 싶은데 귀찮거나, 너무 어려워서 만들지 못하겠다면 npm 홈페이지에 가서 쇼핑하듯 미리 만들어져 있는 패키지를 고를 수 있음

## 라이브러리 관리를 해주어야 하는 이유 🧐

- 라이브러리간의 의존 관계, 특정 라이브러리가 다른 라이브러리 버전에 영향을 받는 경우가 있어 라이브러리 관리를 해주어야 함

  (Ex. jquery-ui는 jquery 버전에 의존적)
## NPM 사용 이유와 장점 👍
예시) 다른 사람들과 협업하며 웹 페이지 개발 진행할 때, 개발에 필요한 라이브러리를 사용하는 경우
### AS-IS
```
// index.html

...
<div></div>
<div></div>
<script src="https://jqery-ui.com/date-picker.js" />
<div class="date-picker"></div>
<div></div>
<div></div>
...
```
- cdn으로 사용하는 경우, 라이브러리 cdn 파일을 검색하며 찾아야 하는 번거로움
- 다른 사람이 사용하는 라이브러리는 script라는 태그를 찾아야함
- 라이브러리에 대한 버전의 정보가 script 태그 안에 명시되어 있음

  → 라이브러리를 관리하는 측면과 의존성이 엮였을 때의 문제점들이 존재하게 됨
### TO-BE
```
// package.json

{
  ...
  "dependencies": {
    "jquery": "^3.4.1",
    "jquery-ui": "^2.1.1"
  }
}
```
-  **장점1**
   - 프로젝트에 사용되는 라이브러리 목록 파악 가능
   - 라이브러리의 정보와 버전을 한눈에 파악 가능

- **장점2**
  ```
  npm install 라이브러리명
  ```
  - 명령어로 설치,관리 및 사용의 간편화

## 기본 명령어 🛠

### node -v
```
node -v
```
  - Node.js 버전 확인

### npm -v
```
npm -v
```
  - NPM 버전 확인

### npm init
```
npm init

// package name: 패키지명
// version: 패키지 버전
// description: 패키지 설명
// entry point: 실행이 시작되는 파일
// ...
```
> entry point? 사용자가 모듈 서비스에 접근할 수 있도록 할 수 있게 해주는 자바스크립트 파일
- 패키지를 정의하는 명령어


  ```
  npm init -y
  ```
  - 기본값을 이용하여 package.json을 바로 생성

### npm install
```
// 명령어
npm install <패키지명>

// 예시
npm install jquery
```
- npm을 이용해서 라이브러리를 설치하는 명령어
  - 설치한 라이브러리는 node_modules 디렉토리 안에 설치가 된다.
- 일반적인 경우, 특정 라이브러리가 설치됐을 때 dist 폴더 밑의 파일들을 참조

## 실습 👩‍💻
1. ### 프로젝트 폴더 생성
  ```
  mkdir npm
  ```

2. ### 프로젝트 폴더로 이동
  ```
  cd npm
  ```
3. ### 프로젝트 초기화
  ```
  npm init -y
  ```
- - -
위의 내용은 NPM을 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 프론트엔드 개발자를 위한 웹팩](https://www.inflearn.com/course/%ED%94%84%EB%9F%B0%ED%8A%B8%EC%97%94%EB%93%9C-%EC%9B%B9%ED%8C%A9)