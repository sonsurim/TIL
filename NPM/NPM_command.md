# NPM 명령어

## 지역 설치 🔏
```
// 축약 형태
npm i <패키지명>

// 기본 형태
npm install <패키지명>

// 예시
npm install gulp
```
- package.json `dependencies` 목록에 추가
- 설치한 패키지 관련 라이브러리가 프로젝트 내 node_modules 디렉토리안에 설치

### 지역 설치 옵션 - Prod
```
// 축약 형태
npm i jquery -D

// 기본 형태
npm install jquery --save-prod
```

### 지역 설치 옵션 - Dev
```
// 축약 형태
npm i jquery -D

// 기본 형태
npm install jquery --save-dev
```
- package.json `devDependencies` 목록에 추가
- 설치한 패키지 관련 라이브러리가 프로젝트 내 node_modules 디렉토리안에 설치
## 전역 설치 🔏
```
// 축약 형태
npm i <패키지명> -g

// 기본 형태
npm install <패키지명> --global

// 예시
npm install gulp --global
```
- **시스템 어딘가에 라이브러리가 설치**
- `npm install`과 동일하게 설치 진행
- 설치는 되었지만 프로젝트 내 node_modules 디렉토리 안에 관련 라이브러리가 설치되지 않음
### 전역 설치를 하는 이유
- 시스템(os) 상에서 명령어를 인식할 수 있게 제공하는 라이브러리들이 존재 (Ex. gulp)

  → 시스템에서 라이브러리에서 제공하는 CLI, 명령어 기능들을 활용하기 위해 전역 설치

### NPM 전역 설치 경로
**- window**
  ```
  %USERPROFILE%\AppData\Roaming\npm\node_modules
  ```

**- mac**
  ```
  /usr/local/lib/node_modules
  ```

### 전역 설치 확인 방법
  ```
  gulp
  // Local gulp not found : gulp라는 명령어를 인식은 하고 있지만 찾지 못함

  gulpp
  // command not found : gulpp 명령어 자체를 인식하지 못함
  ```

## 지역 설치 vs 전역 설치 ⚖️
```
// 지역 설치
npm install jquery
npm install jquery --save-prod
npm i

// 전역 설치
npm install jquery --global
npm install jquery -g
npm i jquery -g
```
### 지역 설치
- 해당 프로젝트의 node_modules에 관련 라이브러리 설치
### 전역 설치
- 시스템 레벨에서 사용할 자바스크립트 라이브러리를 설치할 때 사용
- 시스템 레벨의 node_modeuls에 관련 라이브러리 설치

## 삭제 🔏
```
npm uninstall <패키지명>

npm uninstall gulp
```
- package.json 목록에서 삭제
- 프로젝트 내 node_modules 디렉토리안의 관련된 라이브러리 모두 삭제

- - -
위의 내용은 NPM을 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [인프런 강의 - 프론트엔드 개발자를 위한 웹팩](https://www.inflearn.com/course/%ED%94%84%EB%9F%B0%ED%8A%B8%EC%97%94%EB%93%9C-%EC%9B%B9%ED%8C%A9)