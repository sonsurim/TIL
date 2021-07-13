# Package.json
## 정의 📋
- NPM 패키지에 관한 정보와 의존중인 버전에 대한 정보를 담고 있는 파일
## 특징 🙌
- 프로젝트가 필요로 하는 패키지를 한눈에 파악 가능
## 필요성 🧐
- npm에서 패키지를 사용한다면 실제 서비스에서는 패키지를 수십, 수백 개 가량 다운받게 되기 때문에 각각의 패키지에 대한 버전을 기록해야 함

  → 버전이 중요한 이유?  버전이 업그레이드 되면서 이전  버전과 호환이 안 될 수도 있기 때문

  → 패키지명과 함께 패키지 버전도 함께 기록 필요

## 생성 방법 🔏

1. ### 직접 생성
   - 프로젝트 파일 내에 `package.json` 파일 생성

2. ### npm init 명령어로 생성
    ```
    npm init -y
    ```
    - `-y` : 프로젝트 이름, 버전, 설명, 라이센스 등 모든 옵션에 대해 허용

## 속성 🔩
```
{
  "name": "npm test",
  "version": "7.19.1",
  "description": "surim's github",
  "private": true,
  "keywords": ["surim", "github"],
  "homepage": "https://github.com/sonsurim",
  "bugs": {
    "url": "https://github.com/sonsurim",
    "email": "surim014@naver.com"
  },
  "license": "MIT",
  "author": "Surim <surim014o@naver.com> (https://github.com/sonsurim)",
  "repository": {
    "type": "git",
    "url": "https://github.com/sonsurim"
  },
  "main": "index.js",
  "scripts": {
    "start": "index.js",
  }
  "engines": {
    "node": "16.x",
    "npm": "7.x"
  },
  "dependencies": {...},
  "devDependencies": {...}
}
```
### description, keyword
- 프로젝트의 설명
- 사용자가 검색할 때 쉽게 찾을 수 있게 해줌

### private
- 해당 패키지의 공개/비공개 여부

### bugs
- 버그발생시, 제보할 곳

### author
- 제작자의 정보

### repository
- 해당 코드가 저장되어 있는 곳의 정보

### main
- 패키지의 메인 파일

### script
- 여러가지 npm 명령어

### engines, os, cpu
- 해당 패키지가 특정 환경에서만 동작할 수 있게 하는 속성

### dependencies
- 배포시에도 필요로 하는 패키지
### devDependencies
- 개발 모드일 때만 의존하고 있는 패키지
- 실제로 배포할 때 필요없는 테스트 도구, 웹팩, 바벨같은 것들이 들어감
### peerDependencies
- 직접 require은 하지 않지만 호환되는 패키지 목록
- 주로 패키지의 플러그인 개발할 때 사용

- - -
위 내용은 NPM을 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [제로초 블로그 - package.json](https://www.zerocho.com/category/NodeJS/post/5825a3caaff5c70018279975)